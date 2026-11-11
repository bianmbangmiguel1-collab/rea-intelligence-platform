# Plan d'implémentation — phase 5

**Statut :** plan de mise en œuvre finalisé à titre documentaire. Ce document ne vaut ni validation de recette ni autorisation d'exécution sur cible réelle. Il sert à cadrer la phase 5 et à formaliser les vérifications minimales avant la mise en œuvre.

## 1. Objet

La phase 5 vise la réalisation contrôlée de la plateforme sur la base de la révision REA de référence et des décisions validées des phases 2 à 4. Cette phase doit rester limitée au périmètre documenté, sans extension implicite et sans exécution d'analyse sur cible réelle non autorisée.

## 2. Périmètre autorisé

### 2.1 Inclusions autorisées

- création du squelette applicatif documenté ;
- backend central et modules métier selon la conception validée ;
- interface utilisateur ou façade de contrôle conforme aux exigences ;
- service d'agent local ou runner avec isolation et politique d'autorisation ;
- adaptateur REA isolé, sous révision de référence et sans modification du dépôt externe ;
- contrats de plateforme, journaux, preuve et rapports ;
- tests sécurisés, contrôlés et sans cible réelle par défaut.

### 2.2 Exclusions explicites

- aucune exécution de REA sur une cible réelle non autorisée ;
- aucune exécution automatique de fichiers ou archives importées ;
- aucune collecte ou transfert de données hors périmètre ;
- aucun fournisseur IA non autorisé dans la politique de données ;
- aucun changement de révision REA sans revalidation documentaire ;
- aucun déploiement production tant que la recette de phase 5 n'est pas satisfaite.

## 3. Livrables attendus

1. squelette applicatif minimal conforme à l'arborescence cible ;
2. contracts et modèles de domaine consolidés ;
3. backend central avec gestion des projets, tâches et preuves ;
4. agent local et orchestration des tâches ;
5. gestion de permissions et de preuve ;
6. interfaces de suivi et de rapport ;
7. tests de sécurité, intégration et recette ;
8. procédure d'exploitation et de reprise ;
9. journal de validation et de décision.

## 4. Ordre de mise en œuvre

### Bloc 1 — fondations

- définir les conventions de projet ;
- créer les dossiers applicatifs et le périmètre de travail ;
- établir les dépendances minimales, sans secret ni configuration sensible ;
- choisir les outils de validation autorisés dans le périmètre.

### Bloc 2 — contrats et domaine

- stabiliser les modèles de projet, tâche, preuve et autorisation ;
- normaliser les états de workflow ;
- définir les règles de validation de périmètre et de permissions.

### Bloc 3 — backend et flux

- mettre en place le backend central ;
- gérer l'injection de tâches et la traçabilité ;
- stocker fossiles minimaux et preuves dans un schéma contrôlé ;
- documenter les erreurs et états partiels.

### Bloc 4 — agent et adaptateur

- isoler l'adaptateur REA ;
- définir la frontière d'intégration et la politique d'autorisation ;
- valider le comportement dans un environnement contrôlé ;
- ne pas modifier le dépôt `morluto/rea`.

### Bloc 5 — sécurité et validation

- tests d'autorisation inter-projets ;
- tests d'absence d'exécution automatique ;
- tests d'intégrité et de preuve ;
- revue de journaux, secrets et exfiltration ;
- préparation de la recette de livraison.

## 5. Critères de validation de phase 5

La phase 5 ne peut être déclarée satisfaite qu'après vérification des éléments suivants :

- [ ] le périmètre est conforme au dépôt et aux décisions validées ;
- [ ] la révision REA de référence est utilisée et tracée ;
- [ ] les tests de sécurité sont exécutés et documentés ;
- [ ] les opérations non autorisées sont rejetées par conception ;
- [ ] les journaux, preuves et rapports sont conservés sans secret ;
- [ ] les données traitées restent dans le périmètre déclaré ;
- [ ] la validation du propriétaire est enregistrée avant toute utilisation réelle.

## 6. Risques et garde-fous

- changement de périmètre non documenté ;
- dépendance externe non référencée ;
- fuite de secrets ou exécution non contrôlée ;
- mauvaises hypothèses sur les interfaces REA ;
- tests insuffisants sur la sécurité de l'agent ;
- résultats d'analyse présentés comme faits alors qu'ils ne sont pas validés.

## 7. Décision de clôture

Ce document clôture le plan préparationnel de la phase 5. Il ne remplace ni la validation technique, ni la recette, ni l'approbation explicite du propriétaire. La phase 5 ne peut être déclarée terminée qu'après exécution des tests validés et enregistrement formel de la recette.
