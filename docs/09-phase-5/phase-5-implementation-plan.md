# Plan d'implémentation — phase 5

**Statut :** plan de mise en œuvre documentaire ; réalisation non commencée et phase non validée. Ce document ne vaut ni validation de recette ni autorisation de contourner les consignes actuelles du dépôt.

## 1. Objet

La phase 5 vise la réalisation contrôlée de la plateforme sur la base de la révision REA de référence et des décisions validées des phases 2 à 4. La phase ne peut être clôturée qu'après production des livrables et vérification documentée des critères d'acceptation.

## 2. Périmètre envisagé

Les composants ci-dessous sont des livrables futurs, non présents ni réalisés à la date de cette revue :
- squelette applicatif minimal ;
- contrats et modèles de domaine consolidés ;
- backend central pour projets, tâches et preuves ;
- agent local et orchestration, si autorisés et compatibles ;
- adaptateur REA isolé, sans modification du dépôt externe ;
- journaux, preuves, rapports et tests contrôlés.

Les exclusions restent : pas d'exécution de fichiers importés, pas de cible réelle sans autorisation expresse, pas de transfert IA non approuvé, pas de production avant recette.

## 3. Dépendances et blocages actuels

- `AGENTS.md` autorise actuellement le travail documentaire seulement et interdit explicitement code applicatif, installation, exécution REA, analyse réelle et déploiement.
- Le rapport d'audit disponible épingle `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`, mais identifie plusieurs propriétés d'intégration comme restant à vérifier ; le commit SHA seul n'est pas une matrice d'audit complète.
- Aucun artefact applicatif, résultat de test ou rapport de recette n'est consigné.

Ces points doivent être résolus avant une mise en œuvre ou une validation de phase 5.

## 4. Séquence proposée après levée des blocages

1. Définir les décisions techniques et le périmètre minimal approuvés.
2. Créer le squelette applicatif minimal et les contrats de domaine.
3. Implémenter les fonctions de projet, autorisation, tâches et provenance.
4. Ajouter l'adaptateur REA uniquement après vérification de ses interfaces sur la révision épinglée.
5. Ajouter des tests synthétiques contrôlés, puis les vérifications de sécurité prévues.
6. Consigner les résultats, défauts ouverts, limites et approbation de recette.

## 5. Critères de validation de phase 5

La phase ne peut être déclarée satisfaite qu'après preuve de chacun de ces critères :

- [ ] livrables réalisés et versionnés selon le périmètre approuvé ;
- [ ] intégration traçable à la révision REA auditée et aux sources des interfaces utilisées ;
- [ ] critères fonctionnels exécutés, résultats et écarts consignés ;
- [ ] tests de sécurité exécutés dans un environnement autorisé, avec preuves ;
- [ ] refus des opérations non autorisées démontré ;
- [ ] journaux, preuves et rapports inspectés pour absence de secrets ;
- [ ] flux et conservation des données vérifiés par rapport au périmètre ;
- [ ] défauts et risques résiduels traités ou explicitement acceptés ;
- [ ] validation finale du propriétaire enregistrée après examen des résultats.

## 6. État de la validation

À la date de ce document, aucun critère de réalisation ci-dessus ne dispose d'une preuve de recette dans le dépôt. La phase 5 demeure **non commencée/non validée**. Voir [l'état de validation](phase-5-validation-status.md).
