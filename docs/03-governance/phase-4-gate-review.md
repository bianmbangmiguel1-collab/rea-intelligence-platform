# Porte de phase 4 — revue finale avant réalisation

**Statut :** revue finale de conception clôturée ; la phase 4 est validée pour la suite de la réalisation. Ce document formalise le point de clôture et ne supprime pas les obligations de vérification dans la phase 5.

## 1. Objet de la revue

La phase 4 sert à vérifier que les dépendances de conception sont bien closes, que le pilote et les risques ont été arbitrés, que les approbations nécessaires sont données et que la réalisation est encore rationnelle et maîtrisée.

Aucune implémentation, aucune installation d'outil, aucune exécution REA, aucune analyse sur cible réelle ni aucun déploiement n'est autorisé avant la clôture de cette phase.

## 2. Conditions minimales de clôture

### 2.1 Audit REA

- [x] révision immuable de `morluto/rea` choisie et identifiée ;
- [x] rapport d'audit documenté avec sources datées ;
- [x] matrice des capacités, interfaces, sessions, preuves, erreurs et annulation enregistrée ;
- [x] cas d'usage et limites explicitement distingués entre faits vérifiés et hypothèses.

**Révision retenue :** `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`  
**Source :** https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f

### 2.2 Conception fonctionnelle

- [x] spécification fonctionnelle validée pour le périmètre de pilotage retenu ;
- [x] exigences et critères d'acceptation liés au besoin documentés ;
- [x] états et approbations du produit clairement décrits et conformes au pilote ;
- [x] flux de preuve, rapports et export vérifiés comme cohérents avec les exigences.

### 2.3 Conception sécurité et exploitation

- [x] phase 3 validée par le propriétaire ;
- [x] agents, identités, secrets, données, IA et incidents correctement décrits ;
- [x] risques résiduels listés, affectés à un propriétaire et acceptés ou traités ;
- [x] plan de réponse aux incidents et de reprise défini pour le périmètre réel.

### 2.4 Périmètre pilote et coût

- [x] pilote minimale clairement définie ;
- [x] risques de sécurité, de confidentialité et de licence explicités ;
- [x] coûts, support, disponibilité et trésorerie estimés ;
- [x] critères d'acceptation et de refus de la réalisation établis.

## 3. Vérification de revue finale

Le propriétaire a validé explicitement les éléments suivants :

- [x] le périmètre fonctionnel est stable et cohérent ;
- [x] l'audit REA est complet pour la révision cible ;
- [x] les décisions de sécurité et exploitation sont validées ;
- [x] les dépendances, licences et fournisseurs sont connus ;
- [x] les critères de recette de conception sont définis ;
- [x] les risques résiduels sont acceptés ou maîtrisés ;
- [x] l'autorisation de réalisation est donnée par écrit.

## 4. Décision de sortie

La phase 4 est clôturée avec validation explicite du propriétaire et l'ouverture de la phase 5+ est autorisée sous le périmètre documenté et avec la révision REA de référence retenue.

La réalisation doit s'appuyer sur la révision officielle `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` et respecter les contrôles de sécurité et les critères de recette définis dans les documents du dépôt.

## 5. Conditions de vigilance en phase 5

- toute évolution de périmètre ou de dépendance doit être documentée ;
- toute modification liée à REA ou à un fournisseur externe doit être référencée à la révision utilisée ;
- toute anomalie de sécurité, de preuve ou de performance doit être tracée et reconsidérée avant prolongation du périmètre.
