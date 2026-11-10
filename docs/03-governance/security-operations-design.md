# Conception sécurité et exploitation — version préliminaire

**Statut :** proposition documentaire de phase 3, non validée et non implémentée. Ce document ne clôt ni l'audit REA ni la porte de réalisation. Les choix dépendant du fournisseur, de l'hébergement, de l'OS et du moteur restent ouverts.

## 1. Objectif et principes

Préciser les décisions à prendre pour l'identité des agents, le transport, l'isolation, les secrets, les données, l'exploitation et la réponse aux incidents avant tout déploiement. La conception doit appliquer : refus par défaut, moindre privilège, séparation plan de contrôle/exécution, autorisation explicite par projet/cible/opération, traçabilité, révocation et mode sans IA.

Aucune cible réelle, commande REA ou capacité d'agent n'est autorisée par ce document. Les éléments d'intégration REA sont conditionnés à un audit d'une révision précise.

## 2. Identités, rôles et frontières de confiance

### Proposition de rôles

- **Propriétaire de plateforme :** paramètres globaux, fournisseurs et révocations.
- **Propriétaire de projet :** membres, cibles, autorisations, classification, rétention et approbations du projet.
- **Opérateur :** demande une tâche dans le périmètre accordé ; ne peut pas s'accorder à lui-même une autorisation qu'il ne possède pas.
- **Approbateur :** confirme des actions sensibles séparément de la demande lorsque le risque le requiert.
- **Lecteur :** accès en lecture aux éléments accordés, sans exécution ni modification des permissions.
- **Agent :** identité technique unique, limitée à l'acceptation et à l'exécution de tâches déclaratives autorisées.

Ces rôles sont une proposition ; leur séparation et le modèle d'identité restent à valider selon le pilote.

### Invariants proposés

1. Une identité d'agent ne se confond pas avec une identité utilisateur.
2. Toute requête est autorisée côté serveur pour la ressource et le projet concernés ; l'agent vérifie également l'identité, l'expiration et le périmètre de la tâche reçue.
3. L'agent ne reçoit que les données et permissions indispensables à une tâche spécifique.
4. Aucun secret permanent n'est renvoyé dans une réponse d'enrôlement ou copié dans les journaux.
5. Les actions privilégiées, approbations, changements de politique et révocations sont attribuables et auditées.

## 3. Enrôlement, cycle de vie et révocation des agents

### Flux conceptuel proposé

1. Un administrateur initie un enrôlement temporaire et visible, associé au projet/espace et à une date d'expiration.
2. Le nouvel agent présente la preuve d'enrôlement ; le serveur valide qu'elle est unique, non expirée et non révoquée.
3. Le serveur attribue une identité d'agent propre et enregistre l'environnement, la version déclarée et la date d'observation. Les capacités sont « déclarées », pas « vérifiées », tant qu'une méthode de validation n'est pas définie.
4. Un responsable approuve l'agent avant qu'il puisse recevoir un travail, selon la politique du pilote.
5. Le serveur et l'agent renouvellent périodiquement leur preuve de possession, selon un protocole à choisir après revue des contraintes.
6. Révocation ou expiration bloque immédiatement les nouvelles attributions. Les tâches en cours sont mises en état sûr et signalées ; une déconnexion ne constitue pas une preuve d'arrêt.

### Décisions à prendre

- Durée de validité et méthode d'enrôlement ; limites du mode hors ligne.
- Rotation, stockage local, renouvellement, récupération et révocation des justificatifs.
- Politique d'approbation et nombre de personnes requises pour les opérations sensibles.
- Version minimale de l'agent, compatibilité, mise à jour, signature et retour arrière.
- Traitement d'une capacité inconnue, périmée ou contradictoire.

La méthode cryptographique et le protocole de transport ne sont pas choisis dans ce document. Les secrets ne doivent pas être intégrés au dépôt ou à une tâche journalisée.

## 4. Transport et exécution isolée

### Exigences de conception

- Le canal doit authentifier les deux extrémités, protéger l'intégrité et la confidentialité, limiter le rejeu et rendre les événements corrélables.
- Privilégier un modèle sans écoute de commande entrante sur le poste, sous réserve de faisabilité et d'analyse du risque.
- Les tâches sont des déclarations structurées à schéma fermé ; aucune commande système arbitraire issue de l'interface, d'un fichier cible ou d'un modèle n'est admise.
- Vérifier de nouveau autorisation, expiration, cible, action et politique au point d'exécution ; le backend seul ne suffit pas si l'agent peut recevoir une tâche retardée.
- Les opérations doivent avoir des délais et limites de ressources définis ; les échecs et résultats partiels sont conservés sans être transformés en succès.
- L'espace de travail d'une tâche est séparé des autres tâches ; l'accès réseau, fichiers, processus et secrets est limit�� au besoin autorisé.
- Les contenus de cible et imports restent des données non fiables et ne peuvent pas modifier la politique ni le plan d'exécution.

### Défaillances à traiter explicitement

Perte du canal, réponse répétée, accusé de réception perdu, tâche expirée reçue tardivement, révocation pendant une tâche, indisponibilité du backend, arrêt non confirmé, espace disque épuisé et résultat partiellement remonté. Une reprise doit être bornée, idempotente et ne pas répéter implicitement une opération sensible.

### Décisions ouvertes

Transport, mécanisme d'isolation réellement disponible sur les OS ciblés, contrôle réseau sortant, limites et signification d'une annulation. Aucun de ces points ne peut être considéré comme pris en charge par REA avant audit.

## 5. Secrets et clés

Inventorier les secrets par finalité, propriétaire, emplacement, droit d'accès, durée et procédure de rotation/révocation. À définir avant réalisation :

- stockage protégé sur serveur et agent, selon les capacités documentées des environnements retenus ;
- droits de lecture minimaux et accès d'urgence journalisé ;
- rotation, expiration, révocation, récupération et traitement d'un appareil perdu ;
- masquage avant écriture des logs, erreurs, événements, prompts, rapports et exports ;
- interdiction de placer des clés dans le code, les tâches, les preuves ou les journaux ;
- contrôle des sauvegardes contenant des données chiffrées et des matériaux de récupération.

Aucun mécanisme précis de coffre, KMS ou stockage local n'est accepté à cette étape.

## 6. Données, stockage et cycle de vie

### Catégories à distinguer

Identités et accès ; configuration ; autorisations ; paramètres et événements de tâche ; données source ; preuves et artefacts ; rapports ; appels et sorties IA ; audit et journaux opérationnels ; secrets.

### Exigences proposées

- Accès selon le projet, le rôle et la finalité ; contrôle côté serveur à chaque lecture et export.
- Séparer métadonnées et objets volumineux ; objets privés par défaut et accès temporaire, borné et journalisé si partage autorisé.
- Protéger l'intégrité et conserver empreinte, origine, date, transformations, classification et lien à la tâche lorsque disponibles.
- Définir une durée distincte par catégorie, une règle de gel de conservation si nécessaire, une suppression vérifiable et ses limites dans les sauvegardes.
- Définir région, chiffrement, gestion des clés, accès opérateur, sauvegarde et restauration avant de choisir le fournisseur.
- Prévoir l'export et la suppression sans supprimer silencieusement les traces d'audit nécessaires ; documenter les exceptions et leur base.
- Ne pas inclure de données sensibles dans les métriques ou journaux techniques par défaut.

### Paramètres non décidés

Région, fournisseur, chiffrement au repos/en transit, clés, durées, taille maximale, sauvegardes, objectifs de reprise et processus de suppression. Les exigences juridiques applicables restent à déterminer selon les utilisateurs et territoires concernés.

## 7. Gouvernance IA et fournisseurs externes

L'IA demeure facultative. Avant tout appel ultérieur, la conception devra établir : finalité, données exactes, classification, minimisation/expurgation, consentement habilité, fournisseur/modèle autorisé, coût, rétention et comportement en cas d'indisponibilité. Refuser l'envoi si une condition est manquante ou ambiguë.

Les réponses d'IA sont des contenus dérivés non fiables : elles ne peuvent pas autoriser, approuver ou déclencher une exécution. Le mode sans IA conserve l'accès aux résultats sources. OpenRouter est une option envisagée, pas un fournisseur approuvé ni un flux autorisé.

## 8. Journaux, observabilité et audit

### Journal d'audit proposé

Pour chaque événement pertinent, conserver au minimum : identifiant d'événement, date UTC, acteur, rôle, action, ressource/projet, décision, résultat, raison normalisée, version de politique et identifiant de corrélation. Pour une tâche : demandeur, approbateur éventuel, agent affecté, autorisation, état, versions déclarées, transfert de données, limites et résultat final vérifié.

Ne pas journaliser secrets, contenu source entier ou données personnelles non nécessaires. Les accès aux journaux sont restreints ; toute modification ou export des journaux doit être traçable. Les niveaux de détail, durée et mécanisme de protection contre l'altération restent à décider.

### Santé et alertes à concevoir

Disponibilité des services, agents obsolètes, échecs répétés, files bloquées, dépassement de budget, erreurs fournisseur et révocations. Une alerte ne doit pas exposer de contenu sensible. Les seuils et canaux d'alerte sont à fixer avec le pilote.

## 9. Réponse aux incidents

### Procédure conceptuelle

1. Détecter, enregistrer l'heure et préserver le contexte sans propager des données sensibles.
2. Évaluer portée, projets, agents, tâches, preuves et fournisseurs concernés.
3. Contenir : suspendre l'attribution, révoquer l'agent ou l'accès, bloquer un transfert/fournisseur, selon le cas.
4. Vérifier l'état réel des tâches ; signaler comme interrompues/inconnues celles dont l'arrêt n'est pas prouvé.
5. Préserver les preuves utiles avec accès restreint et chaîne de provenance.
6. Évaluer obligations de notification et de communication ; les responsables et délais restent à définir selon le contexte légal et opérationnel.
7. Restaurer depuis une source de confiance, renouveler les secrets concernés et surveiller une récidive.
8. Revoir la cause, les risques et les contrôles ; documenter actions et décision de réouverture.

Aucun plan d'urgence n'est considéré opérationnel avant attribution de responsables, canaux de contact, critères de gravité et exercice ultérieur autorisé.

## 10. Exploitation et gestion des changements

Avant mise en service, choisir et documenter : environnements distincts ; propriétaires opérationnels ; configuration sans secret dans Git ; inventaire et provenance des dépendances ; traitement des vulnérabilités ; mises à jour et retour arrière ; sauvegardes/restauration ; quotas et limites de coûts ; support et fin de vie des versions.

Chaque changement d'agent, de dépendance, de moteur REA, d'API, de fournisseur IA ou de politique doit identifier la version, les tests requis, les impacts, la décision d'approbation et les conditions de retour arrière. Une mise à jour REA ne doit pas être adoptée silencieusement : elle déclenche une revue de compatibilité.

## 11. Plan de vérification futur — non exécuté

Après autorisation séparée de la réalisation, préparer des vérifications en environnement contrôlé et sans cible réelle par défaut :

- autorisation inter-projets et refus des périmètres absents/expirés ;
- enrôlement unique, expiration, rotation et révocation ;
- tâche rejouée, retardée, annulée ou interrompue ; absence de faux succès ;
- isolation et refus de permissions non requises ;
- ressources importées non exécutées avant approbation ;
- expurgation des secrets dans erreurs et journaux ;
- contrôle des transferts IA, consentements, budget et mode sans IA ;
- accès aux preuves, intégrité, export, rétention et suppression ;
- restauration vérifiée et procédure d'incident ;
- compatibilité et adaptation uniquement sur version REA auditée.

Les cas, critères de réussite, responsables, preuves et environnements devront être approuvés avant exécution. Aucun contrôle de ce plan n'a été exécuté par la rédaction.

## 12. Décisions restant à valider

1. Portée et rôles du pilote, responsables et approbations.
2. Transport agent, isolation, OS et stratégie hors ligne.
3. Fournisseurs d'identité, hébergement, stockage, régions et gestion de clés.
4. Données permises, rétention, sauvegardes, suppression et obligations applicables.
5. Fournisseur IA, consentement et catégories de données transférables.
6. Objectifs de reprise, disponibilité, budget, support et gestion d'incident.
7. Critères d'acceptation, risques résiduels et portée des essais autorisés.

## Porte de phase 3

La phase ne peut être déclarée terminée qu'après examen de chaque décision, attribution d'un propriétaire et d'un statut, traitement des risques bloquants, définition des vérifications et validation explicite du propriétaire du projet. Ce document seul ne satisfait pas cette porte.
