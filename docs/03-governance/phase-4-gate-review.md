# Porte de phase 4 — revue finale avant réalisation

**Statut :** document de préparation de la porte avant réalisation. Il formalise les éléments à vérifier avant toute mise en œuvre et ne vaut pas autorisation de démarrer le développement.

## 1. Objet de la revue

La phase 4 sert à vérifier que les dépendances de conception sont bien closes, que le pilote et les risques ont été arbitrés, que les approbations nécessaires sont données et que la réalisation est encore rationnelle et maîtrisée.

Aucune implémentation, aucune installation d'outil, aucune exécution REA, aucune analyse sur cible réelle ni aucun déploiement n'est autorisé avant la clôture de cette phase.

## 2. Conditions minimales de clôture

### 2.1 Audit REA

- révision immuable de `morluto/rea` choisie et identifiée ;
- rapport d'audit documenté avec sources datées ;
- matrice des capacités, interfaces, sessions, preuves, erreurs et annulation enregistrée ;
- cas d'usage et limites explicitement distingués entre faits vérifiés et hypothèses.

### 2.2 Conception fonctionnelle

- spécification fonctionnelle validée pour le périmètre de pilotage retenu ;
- exigences et critères d'acceptation liés au besoin documentés ;
- états et approbations du produit clairement décrits et conformes au pilote ;
- flux de preuve, rapports et export vérifiés comme cohérents avec les exigences.

### 2.3 Conception sécurité et exploitation

- phase 3 validée par le propriétaire ;
- agents, identités, secrets, données, IA et incidents correctement décrits ;
- risques résiduels listés, affectés à un propriétaire et acceptés ou traités ;
- plan de réponse aux incidents et de reprise défini pour le périmètre réel.

### 2.4 Périmètre pilote et coût

- pilote minimale clairement définie ;
- risques de sécurité, de confidentialité et de licence explicités ;
- coûts, support, disponibilité et trésorerie estimés ;
- critères d'acceptation et de refus de la réalisation établis.

## 3. Vérification de revue finale

Le propriétaire doit confirmer explicitement les éléments suivants :

- [ ] le périmètre fonctionnel est stable et cohérent ;
- [ ] l'audit REA est complet pour la révision cible ;
- [ ] les décisions de sécurité et exploitation sont validées ;
- [ ] les dépendances, licences et fournisseurs sont connus ;
- [ ] les critères de recette de conception sont définis ;
- [ ] les risques résiduels sont acceptés ou maîtrisés ;
- [ ] l'autorisation de réalisation est donnée par écrit.

## 4. Cas de refus de la porte

La phase 4 reste bloquée si l'un des éléments suivants subsiste :

- révision REA non choisie ou non auditée ;
- approbation fonctionnelle ou sécurité insuffisante ;
- périmètre pilote non défini ou non maîtrisé ;
- faute de preuve sur le transport, l'isolation ou la gestion des secrets ;
- fournisseur IA non autorisé ;
- risque résiduel non signé par un responsable ;
- absence d'autorisation écrite du propriétaire.

## 5. Décision de sortie

La phase 4 n'est clôturée qu'après validation explicite du propriétaire et enregistrement de la décision, ce qui ouvre la phase 5+ uniquement dans le cadre d'un périmètre documenté et accepté.

Jusqu'à cette validation, le projet demeure en phase de conception, avec réalisation interdite.
