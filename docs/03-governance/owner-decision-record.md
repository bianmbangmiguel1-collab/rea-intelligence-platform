# Registre des décisions du propriétaire

**Statut :** support de décision à compléter. Aucune option ci-dessous n'est acceptée ou autorisée par défaut. Les propositions documentaires restent des propositions jusqu'à validation explicite du propriétaire.

Ce registre transforme les arbitrages ouverts de la [revue de phase](phase-review.md) en décisions traçables. Il ne clôt aucune phase, ne remplace pas l'audit REA et ne vaut pas autorisation de réaliser ou d'analyser une cible.

## Comment consigner une décision

Pour chaque entrée, le propriétaire peut inscrire une décision ou laisser la question ouverte. En cas de décision, préciser les alternatives examinées, la justification, les conséquences, les limites, le risque résiduel, le responsable et la date. Référencer les preuves avec une source et une révision identifiables. Ne pas inscrire comme fait vérifié une hypothèse REA.

Statuts possibles : **à décider**, **proposé** (sans approbation), **accepté par le propriétaire**, **remplacé**. « Accepté » doit inclure le nom du décideur et la date. Une décision dépendant de l'audit REA reste conditionnelle jusqu'à vérification sur la révision retenue.

## D-01 — Pilote et utilisateurs

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quel est le pilote minimal, qui l'utilisera et quels parcours sont prioritaires ?
- **À préciser :** usage personnel ou autre ; profils et séparation éventuelle des rôles ; cas d'usage inclus et exclus ; résultat attendu ; critères permettant de dire que le pilote répond au besoin.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-02 — Révision et limites de l'audit REA

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quelle révision immuable du dépôt externe `morluto/rea` sera la référence d'audit ?
- **À préciser :** identifiant de commit ou autre référence immuable ; sources à examiner ; périmètre de l'examen documentaire ; opérations autorisées séparément, le cas échéant ; exclusions et règles de licence. Aucun test, installation ou exécution n'est autorisé par le présent registre.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-03 — Cibles et opérations permises

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quelles cibles et catégories d'opérations sont dans le périmètre du pilote, et quelles sont explicitement interdites ?
- **À préciser :** preuve et portée de l'autorisation ; propriétaire de cible ; durée ; exclusions ; conditions de renouvellement ; opérations nécessitant une approbation distincte ; traitement des cibles hors périmètre.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-04 — Approbations, états et annulation

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quelles catégories d'opérations exigent une approbation humaine, et quel comportement est attendu lors d'un refus, d'une erreur ou d'une annulation ?
- **À préciser :** approbateur autorisé ; informations visibles avant approbation ; délai et expiration ; séparation entre demandeur et approbateur si nécessaire ; états de plateforme à retenir ; distinction entre arrêt demandé et arrêt confirmé. Les états proposés dans les spécifications ne sont pas un contrat REA vérifié.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-05 — Déploiement, identité et agents

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quel modèle d'hébergement, d'identité, de transport, d'isolation et de cycle de vie des agents convient au pilote ?
- **À préciser :** responsabilités opérateur/fournisseur ; OS ciblés et preuves de compatibilité requises ; enrôlement ; justificatifs, expiration et révocation ; mises à jour ; fonctionnement hors ligne ; région et frontières réseau. Windows prioritaire et architecture hybride restent des orientations à confirmer.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-06 — Données, IA et conservation

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quelles données peuvent être conservées, exportées ou transmises à un fournisseur externe, et sous quelles conditions ?
- **À préciser :** classification par type ; minimisation ; fournisseur(s) et région ; consentement ; données interdites ; rétention et suppression ; sauvegarde/restauration ; mode sans IA ; budget et réaction au dépassement. OpenRouter reste une option envisagée, non une décision ni une autorisation de transfert.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-07 — Objectifs du pilote et exploitation

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quels seuils mesurables, coûts et engagements d'exploitation sont nécessaires au pilote ?
- **À préciser :** performance ; disponibilité ; limites de taille et de durée ; budget ; support ; observabilité ; objectifs de reprise ; vérifications attendues et critères de recette. Ne pas inscrire de seuil par défaut sans besoin validé.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## D-08 — Risques résiduels et acceptation

- **Statut :** à décider
- **Décideur / date :** à compléter
- **Question :** quels risques résiduels peuvent être acceptés, par qui, pour quelle durée et avec quelle justification ?
- **À préciser :** référence au registre des risques ; traitement ou réduction ; propriétaire du risque ; déclencheurs de réexamen ; risque non acceptable bloquant le passage de phase.
- **Décision / justification :** à compléter
- **Conséquences, dépendances et risque résiduel :** à compléter

## Vérification de complétude avant revue finale

- [ ] Les décisions acceptées identifient le propriétaire, la date et leur justification.
- [ ] Les propositions non validées et questions ouvertes restent clairement distinguées.
- [ ] Les choix dépendant de REA référencent une révision et des éléments d'audit sourcés, ou restent explicitement ouverts.
- [ ] Le périmètre d'autorisation, les exclusions et les opérations interdites sont explicites.
- [ ] Les risques résiduels ont un responsable et un traitement ou une acceptation documentée.
- [ ] Les critères de passage de phases sont satisfaits et la validation explicite du propriétaire est consignée avant toute décision de réalisation.
