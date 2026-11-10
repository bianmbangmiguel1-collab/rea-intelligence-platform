# Revue documentaire sécurité — phase 3

**Statut :** revue de conception et de couverture documentaire effectuée ; approbation du propriétaire **en attente**. Ce document n'est ni un audit de sécurité technique, ni un test, ni une certification de sécurité. Aucun code, agent, moteur REA ou système déployé n'a été examiné en exécution.

## Portée

Documents examinés : modèle de menace initial, conception sécurité/exploitation, architecture détaillée, spécification fonctionnelle, gouvernance données/IA, registre des risques, modèle de données, contrats API et roadmap. La revue vérifie la présence des sujets et la cohérence des contrôles proposés ; elle ne prouve pas qu'ils sont mis en œuvre ou efficaces.

## Résumé de l'avis

La conception documentaire reconnaît les principaux actifs et menaces et pose des garde-fous importants : autorisation explicite, moindre privilège, tâches déclaratives, quarantaine, IA facultative, provenance, révocation et distinction entre interruption et réussite. Les principaux mécanismes opérationnels, responsables, paramètres, critères mesurables et preuves de test ne sont pas encore décidés. Avis : **base de conception acceptable pour poursuivre la revue, mais sécurité non validée et réalisation bloquée**.

## Revue de couverture des contrôles

| Domaine | Contrôle envisagé | État de conception | Reste avant validation |
| --- | --- | --- | --- |
| Autorisation et périmètre | Autorisation datée liée à la cible, aux opérations, exclusions et acteur ; revalidation | Exigence présente dans spécification et architecture | Définir preuve acceptée, politique, règles et critères de refus ; tests futurs requis |
| Séparation des projets | Contrôle d'accès serveur pour chaque ressource et export | Présent dans contrats et architecture | Modèle d'identité/autorisation détaillé ; tests d'accès croisé futurs |
| Réseau et destinations | Contrôle au point d'exécution, redirections et destinations prévues | Risque identifié | Algorithme, limites, politiques et compatibilité d'agent ouverts ; validation technique future |
| Imports et archives | Quarantaine, limites, inspection, aucune exécution automatique | Exigence claire | Formats, isolation, responsabilité, taille et critères d'approbation à définir |
| Exécution et commandes | Schéma fermé ; refus des commandes arbitraires ; privilèges minimaux | Principe explicite | Inventaire d'opérations permis et mapping REA après audit ; vérifications futures |
| Agent et identifiants | Identité unique, enrôlement temporaire, expiration, rotation et révocation | Flux préliminaire décrit | Mécanisme/protocole, durées, responsabilités, mise à jour et mode hors ligne ouverts |
| Transport | Authentification, intégrité, confidentialité, résistance au rejeu | Objectif exprimé | Transport et mécanismes non choisis ; compatibilité non démontrée |
| Isolation | Workspace séparé, restrictions réseau/fichiers/processus et limites ressources | Exigence formulée | Technologie/garanties OS et modèle de menace résiduel à établir |
| Secrets | Pas de secrets dans code, tâches, logs, rapports ou prompts ; rotation | Exigences présentes | Coffre, stockage local, clés, accès d'urgence et procédure de récupération à choisir |
| Données et stockage | Accès minimal, intégrité/provenance, objets privés, rétention et suppression | Principes et catégories documentés | Région, chiffrement, durées, sauvegarde/restauration et suppression à décider |
| Fournisseurs IA | Pas de transfert implicite ; minimisation, consentement et mode sans IA | Gouvernance dédiée et exigence explicite | Fournisseur, catégories permises, conditions, rétention et consentement à valider |
| Journaux/observabilité | Corrélation et audit des actions ; expurgation des secrets | Schéma conceptuel proposé | Protection contre altération, niveaux d'accès, seuils et rétention à définir |
| Résilience | Idempotence, états explicites, reprise bornée, résultats partiels | Principes formulés | Sémantique de reprise/annulation et preuves d'état à détailler, REA à auditer |
| Réponse aux incidents | Contenir, révoquer, préserver, restaurer, revoir | Procédure conceptuelle rédigée | Responsables, canaux, gravité, notification et exercice à définir |
| Supply chain/licences | Épingler les versions, vérifier provenance et licences | Risque reconnu | Audit REA, inventaire dépendances et processus de mise à jour ouverts |
| Exploitation et coûts | Environnements, budgets, mises à jour, sauvegardes et responsabilités | Agenda et proposition rédigés | Hébergement, objectifs de reprise, limites et coûts à arbitrer |

## Risques qui maintiennent la porte bloquée

- Absence d'une révision de référence et d'un audit REA sourcé : capacités, permissions et surfaces d'exécution inconnues.
- Absence de choix validé pour identité/enrôlement/révocation, transport et isolation de l'agent.
- Règles d'autorisation, de périmètre, d'approbation et d'accès inter-projets non détaillées au niveau testable.
- Région, rétention, sauvegardes, suppression, clés et responsabilités d'hébergement non arbitrées.
- Transferts IA et conditions fournisseur non autorisés ni définis.
- Réponse aux incidents sans responsables désignés ni processus opérationnel approuvé.

Ces points ne sont pas déclarés acceptés. Chaque risque doit avoir un propriétaire, une évaluation, un traitement et une preuve avant fermeture ou acceptation formelle.

## Vérifications requises ultérieurement

Après autorisation séparée de réaliser le logiciel, les contrôles décrits dans [la conception sécurité](../02-architecture/security-design.md) et [l'agenda de phase 3](phase-3-design-agenda.md) devront être convertis en cas de test, conditions, jeux de données sûrs, critères de réussite, responsables et preuves. Aucun test de contrôle d'accès, SSRF, archive, secret, révocation, restauration ou transfert IA n'a été exécuté dans cette revue.

## Décision de revue

**Avis documentaire :** couverture de conception préliminaire adéquate pour continuer l'analyse et la revue du propriétaire ; pas d'affirmation que le système est sécurisé, conforme ou prêt. Le risque global reste indéterminé tant que l'audit et les choix ouverts ne sont pas clos.

| Validation | État | Validateur / date |
| --- | --- | --- |
| Revue documentaire de couverture et cohérence | Effectuée dans le cadre de cette tâche | Assistant / 2026-11-10 |
| Validation sécurité du propriétaire | En attente | À renseigner par le propriétaire |
| Audit technique / tests d'efficacité | Non effectués | Prérequis et phase de réalisation ultérieurs |
