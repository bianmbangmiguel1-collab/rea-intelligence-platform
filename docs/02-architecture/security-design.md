# Conception sécurité — modèle de menace initial

**Statut :** première analyse conceptuelle, à compléter avant toute réalisation et à vérifier contre les capacités du moteur et de l'environnement.

## 1. Actifs à protéger

- fichiers sources, binaires, archives et secrets d'analyse ;
- preuves, journaux, rapports et métadonnées de projet ;
- clés IA, jetons d'agent et identifiants d'utilisateur ;
- intégrité de la machine d'analyse et de son réseau ;
- autorisations et limites de périmètre ;
- provenance et historique des décisions.

## 2. Principaux acteurs de menace

- fichier ou archive soumis malveillant ;
- contenu web analysé contrôlé par un tiers ;
- compte utilisateur compromis ou erreur d'opérateur ;
- agent volé, obsolète ou compromis ;
- fournisseur externe ou configuration mal appliquée ;
- panne ou défaut de normalisation entraînant une perte de preuve.

## 3. Menaces et contrôles de conception

| Menace | Contrôles exigés |
| --- | --- |
| Accès hors périmètre | Autorisation explicite, échéance, exclusions, validation côté serveur et agent |
| SSRF / accès réseau non prévu | Politique de destinations, résolution IP contrôlée et revalidation des redirections au point d'exécution |
| Fichier malveillant | Quarantaine, limites de taille, workspace séparé, sandbox et temps CPU/mémoire plafonnés |
| Zip Slip / liens dangereux | Normalisation des chemins, refus des chemins sortants et symlinks non approuvés, inspection avant extraction |
| Exécution arbitraire | Schémas d'opérations fermés, aucune commande shell arbitraire, approbation et liste d'outils permise |
| Compromission d'agent | Identité unique, secrets renouvelables/révocables, moindre privilège, restriction réseau et détection de version |
| Fuite vers IA externe | Consentement/politique par projet, minimisation, filtrage, affichage de destination, mode sans IA |
| Altération/perte de preuves | Empreintes, contenu source séparé des synthèses, journal de provenance et sauvegardes testées |
| Instruction malveillante dans une cible | Traiter le contenu analysé comme donnée non fiable ; modèle sans pouvoir d'exécution/autorisation |
| Ressource importée dangereuse | Quarantaine, inventaire et approbation humaine avant activation ; aucune exécution automatique |

## 4. Autorisations

Une analyse requiert une permission vérifiable qui lie au minimum : demandeur, projet, cible, périmètre, catégories d'opérations, validité temporelle et approbateur. Les opérations sensibles sont soumises à une confirmation distincte. L'expiration ou la révocation invalide les nouveaux travaux ; les traces déjà produites restent accessibles selon la politique de rétention.

## 5. Secrets et transport

Les secrets ne doivent jamais être inclus dans les tâches journalisées, rapports ou prompts. Le canal agent-backend doit authentifier l'agent et protéger l'intégrité/confidentialité du transport ; le mécanisme concret (certificats, jetons courts ou autre) reste à sélectionner. Enrôlement, rotation, révocation, mises à jour et récupération après perte de secret doivent être spécifiés avant développement.

## 6. Stockage et rétention

Définir avant production : classification des données, chiffrement et contrôle des clés, durée de conservation par type, suppression vérifiable, sauvegarde/restauration, liens temporaires d'artefact et audit des accès. La rétention ne doit pas être inventée par défaut : elle est une décision ouverte.

## 7. Réponse aux incidents

Prévoir désactivation d'un agent, révocation de sessions, suspension des jobs, blocage d'un fournisseur IA, conservation des traces nécessaires et revue des artefacts potentiellement exposés. Les procédures opérationnelles et responsabilités restent à détailler.

## 8. Vérifications de sécurité avant implémentation

- revue du modèle de menace et des frontières de confiance ;
- tests de contrôle d'accès inter-projets ;
- tests de validation du périmètre et de SSRF ;
- tests d'archives malformées et de chemins ;
- validation de l'absence de commande arbitraire ;
- essais de révocation et d'expiration d'agent ;
- vérification des journaux expurgés ;
- test de sauvegarde, restauration et suppression ;
- revue des transferts et politiques fournisseurs IA.

Ces éléments sont des exigences de recette de conception ; aucun test n'a été exécuté à cette phase.