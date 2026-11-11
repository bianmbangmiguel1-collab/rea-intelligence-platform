# Brief de décision — phase 3 sécurité et exploitation

**Statut :** document de préparation de décision, non vérifié ni approuvé. Il organise la suite de la phase 3 et ne remplace ni l'audit REA ni l'autorisation de réalisation.

## Objet

Cette note transforme la phase 3 en liste de décisions testables, avec les choix de conception proposés pour le pilote, les agents, les données, l'IA et la gouvernance opérationnelle. Les options ci-dessous sont des propositions de travail, à confirmer par le propriétaire avant toute validation finale.

Les règles applicables sont celles du projet :
- distinguer exigences, choix acceptés, propositions et hypothèses ;
- ne pas traiter REA comme vérifié sans révision et sources identifiées ;
- ne pas autoriser implémentation, exécution de cible réelle ou déploiement tant que la phase 4 n'est pas franchie.

## 1. Décisions de pilotage et de périmètre

### D3-01 — Pilote minimal

**Proposition :** pilote personnel, unique opérateur, un seul projet principal, avec possibilité d'extension sans changement de fond. L'objectif est de valider le flux complet de création de projet, autorisation, exécution, preuve et rapport, sans supposer un usage multi-utilisateur commercial.

**À confirmer :**
- rôle unique ou séparation minimale entre opérateur et approbateur ;
- périmètre autorisé de cibles et types d'actions ;
- exclusions explicites ou hors périmètre ;
- seuil de confidentialité et de criticité des données à traiter.

### D3-02 — Types de cibles et opérations

**Proposition :** commencer avec des cibles web et fichiers locaux de faible criticité, sans accès aux réseaux privés, sans opérations destructrices et sans exécution automatiques sur contenu importé.

**À confirmer :**
- cibles autorisées ou interdites ;
- limites de liens, redirections et accès réseau ;
- catégories d'actions conformes (lecture, collecte, analyse, export) ;
- opérations hors périmètre.

## 2. Décisions de sécurité des agents

### D3-03 — Modèle d'identité et d'enrôlement

**Proposition :** un agent reçoit une identité technique unique, admise par le backend avec preuve d'enrôlement, date d'expiration et capacité d'annulation. L'enrôlement est temporaire et ne se confond pas avec l'identité utilisateur.

**À confirmer :**
- durée de validité ;
- validité de l'agent par projet ou par plateforme ;
- approbation minimale avant affectation ;
- mécanisme de rotation et de révocation.

### D3-04 — Transport et isolation

**Proposition :** canal authentifié bidirectionnel, intégrité garantie, pas d'écoute de commande entrante sur le poste, tâches déclaratives et workload isolé à l'espace de travail de la tâche.

**À confirmer :**
- protocole exact de transport ;
- mécanisme d'isolation disponible sur Windows et Linux ;
- restrictions réseau, fichiers, processus et mémoire ;
- signalement d'une tâche interrompue ou expirée.

### D3-05 — Secrets et stockage local

**Proposition :** pas de secret dans le dépôt, les journaux, les tâches, les prompts ni les sorties d'IA. Les secrets d'agent sont stockés uniquement dans un support protégé et sont rotatifs.

**À confirmer :**
- stockage local ou distant ;
- rotation et récupération ;
- procédures d'urgence et révoquation ;
- accès d'administration et journalisation restreinte.

## 3. Décisions de données et de gouvernance IA

### D3-06 — Classification et rétention

**Proposition :** distinguer au minimum : métadonnées, preuves, artefacts, journaux, exports, résultats d'IA et fichiers sources. Les données sensibles restent privées par défaut.

**À confirmer :**
- classification par catégorie ;
- durée de conservation par type ;
- suppression vérifiable et exception pour les traces d'audit ;
- règles de gel, de sauvegarde et de restauration.

### D3-07 — Fournisseur IA et mode sans IA

**Proposition :** le système doit être conçu pour fonctionner sans appel externe à l'IA. Tout fournisseur externe, y compris OpenRouter, est une option de configuration secondaire, non une exigence ni une validation implicite.

**À confirmer :**
- fournisseur retenu, s'il y a lieu ;
- consentement, minimisation, filtrage et budgets ;
- catégories de données transférables ;
- mode sans IA par défaut.

## 4. Décisions de fonctionnement et de risques

### D3-08 — Observabilité et réponse aux incidents

**Proposition :** chaque action importante doit être corrélée à un projet, une tâche, un acteur, une politique et un résultat. Les incidents sont traités par suspension d'un agent ou d'un accès, puis par restauration avec preuve de la cause.

**À confirmer :**
- niveaux d'alerte ;
- responsables de triage ;
- délais de notification ;
- procédure de réouverture ou de clôture.

### D3-09 — Critères de recette de conception

**Proposition :** avant toute réalisation, les tests suivants doivent être explicitement définis et validés :
- refus d'une tâche sans autorisation valable ;
- refus d'un accès inter-projets ;
- validation de périmètre, d'URL et de redirection ;
- zéro exécution automatique après import de fichier ou archive ;
- rotation, expiration et révocation d'agent ;
- journalisation sans secrets ;
- restauration sur base de preuve ;
- mode sans IA non bloquant pour les résultats techniques.

**À confirmer :**
- environnement de test ;
- responsables ;
- seuils d'acceptation ;
- preuve de conformité de chaque contrôle.

## 5. État des décisions

| Domaine | Proposition | Statut | Note |
| --- | --- | --- | --- |
| Pilote minimal | Personne unique / usage personnel extensible | Proposé | À valider |
| Cibles et opérations | Périmètre limité, sans actions destructrices ni accès réseau non prévu | Proposé | À valider |
| Enrôlement agent | Identité unique + expiration + révocation | Proposé | À valider |
| Transport et isolation | Authentification, tâches déclaratives, workspace isolé | Proposé | À valider |
| Secrets | Aucun secret dans dépôt ou journaux | Proposé | À valider |
| Données | Classification, rétention et suppression documentées | Proposé | À valider |
| IA externe | Mode sans IA obligatoire ; fournisseur optionnel | Proposé | À valider |
| Incidents | Suspension, preuve, restauration, revue | Proposé | À valider |
| Recette | Contrôles de sécurité documentés avant réalisation | Proposé | À valider |

## 6. Décision de phase 3

La phase 3 peut être poursuivie dans le cadre documentaire tant que chaque décision ci-dessus reste explicitement ouverte et attribuée à un propriétaire. La phase n'est pas close tant que :
- l'audit REA n'a pas de révision immuable et de rapport sourcé ;
- les décisions de sécurité et d'exploitation n'ont pas été validées par le propriétaire ;
- les critères de validation de conception ne sont pas formalisés.

Ce document n'autorise ni le développement, ni l'analyse de cible réelle, ni l'exécution du moteur REA. Il sert à préparer la prochaine porte de décision avant réalisation.
