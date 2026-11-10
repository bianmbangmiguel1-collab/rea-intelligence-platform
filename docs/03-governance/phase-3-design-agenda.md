# Agenda de conception — phase 3 sécurité et exploitation

**Statut :** travail à faire. Cette liste organise la conception uniquement ; elle ne décrit pas une configuration implémentée ni une opération autorisée.

## 1. Identité, enrôlement et révocation des agents

- Définir le modèle d'identité unique, l'approbation d'enrôlement et la durée des justificatifs.
- Préciser rotation, expiration, révocation, récupération et comportement hors ligne.
- Définir l'autorité sur l'attribution, l'accusé de réception et la preuve d'arrêt.
- Établir la mise à jour de l'agent, compatibilité, retour arrière et gestion d'un agent obsolète.
- Évaluer Windows en priorité et les autres plateformes uniquement avec preuves de compatibilité.

## 2. Transport et isolation

- Décider le modèle de connexion, authentification mutuelle, intégrité et protection contre la répétition.
- Définir frontières de réseau, destinations autorisées, contrôles au point d'exécution et prévention d'accès non prévu.
- Spécifier isolation de workspace, permissions locales et limites de ressources.
- Ne pas retenir un transport ou un mécanisme REA avant audit ; préciser les responsabilités respectives de l'adaptateur et de l'agent.

## 3. Secrets et clés

- Inventorier secrets, propriétaires, accès, stockage, rotation, révocation et récupération.
- Établir les règles de non-exposition dans journaux, prompts, rapports, dumps et support.
- Documenter gestion des clés et limites de responsabilité des services hébergés.

## 4. Données, stockage et cycle de vie

- Classifier métadonnées, sources, preuves, artefacts, journaux et exports.
- Décider chiffrement, région, contrôle d'accès, rétention par type et suppression vérifiable.
- Définir sauvegarde, restauration, objectifs de récupération et preuve périodique ultérieure.
- Définir les liens de partage et exports protégés, sans URL publique persistante.

## 5. Observabilité et réponse aux incidents

- Champs d'audit et corrélation ; expurgation et accès aux journaux.
- Détection et triage des événements ; suspension de jobs et révocation d'agent/fournisseur.
- Conservation proportionnée des preuves, notification, responsabilités et retour à un état sûr.
- Procédure de revue d'incident et critères de réouverture des risques.

## 6. Exploitation et coûts

- Modèle d'hébergement et responsabilités, environnements et séparation des configurations.
- Limites, budgets, sauvegardes, dépendances, mises à jour et gestion des vulnérabilités.
- Disponibilité et objectifs de reprise alignés sur les besoins du pilote.
- Licences, conditions des fournisseurs et coûts récurrents examinés avant porte de réalisation.

## Critère de sortie

Pour chaque section : décision acceptée ou question ouverte nommée, risque associé, propriétaire, contrôle décrit, scénario de défaillance et moyen de validation ultérieur. Une liste remplie sans revue ni validation ne clôt pas la phase 3.
