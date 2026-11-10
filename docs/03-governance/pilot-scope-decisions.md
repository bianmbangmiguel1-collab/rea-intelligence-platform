# Décisions de cadrage — pilote phase 3

**Statut :** proposition documentaire préparée le 2026-11-10 ; approbation explicite du propriétaire du projet requise. Les éléments ci-dessous ne valent ni validation de sécurité, ni autorisation d'exécuter REA ou d'analyser une cible, ni autorisation de réalisation.

## 1. Proposition de périmètre minimal du pilote

| Sujet | Proposition à valider | Limite / statut |
| --- | --- | --- |
| Mode d'usage | Usage personnel, mono-propriétaire, sans comptes invités ni service multi-tenant | Proposition ; à confirmer par le propriétaire |
| Cible | Uniquement systèmes de laboratoire ou appareils appartenant à l'utilisateur, ou couverts par une autorisation écrite explicite et limitée | Aucune cible réelle n'est autorisée par ce document |
| Cas d'usage | Étude documentaire et expérimentation contrôlée ; collecte et présentation de résultats non destructifs uniquement après autorisation séparée et porte de réalisation applicable | L'audit REA et toute expérimentation restent à autoriser séparément |
| Portée | Une tâche doit être liée à un projet, une cible, une finalité, une fenêtre de validité et des exclusions explicitement consignées | Refus par défaut si une donnée de portée manque ou est ambiguë |
| Données | Données synthétiques ou de laboratoire de préférence ; données personnelles, secrets et données de tiers exclus du pilote initial | Aucune transmission à un service IA autorisée ; mode sans IA obligatoire par défaut |
| Plateformes | Windows envisagé en priorité, sans déclaration de compatibilité avant audit et validation | Hypothèse de cadrage, pas un fait vérifié |
| Multi-utilisateur | Exclu du pilote initial ; pas de partage public ni d'accès inter-projets | Toute extension nécessite une nouvelle décision et une revue |

### Opérations proposées comme permises sous autorisation explicite ultérieure

- Consulter la documentation et les sources d'une révision REA épinglée dans le cadre de l'audit autorisé.
- Décrire des exigences et préparer des scénarios de vérification documentaires, sans les exécuter.
- Après franchissement des portes applicables, envisager des opérations de lecture/non destructives sur un laboratoire explicitement autorisé, limitées au périmètre approuvé et aux capacités préalablement auditées.

Cette liste ne constitue pas une autorisation d'exécuter ces opérations maintenant.

### Opérations exclues du pilote proposé

- Toute cible publique, tierce ou non explicitement autorisée ; toute découverte ou extension automatique du périmètre.
- Toute action destructive, modification persistante, exploitation, élévation de privilèges, contournement de contrôle, persistance, collecte ou extraction d'identifiants, mouvement latéral ou déni de service.
- Toute commande système arbitraire, exécution automatique de fichiers/imports non fiables, ou action déclenchée par une sortie IA.
- Toute exécution REA, installation d'outils, analyse sur cible réelle, déploiement ou code applicatif avant satisfaction des portes du projet et autorisation distincte.
- Tout transfert de données vers OpenRouter ou un autre fournisseur IA tant que données autorisées, consentement, rétention et fournisseur n'ont pas fait l'objet d'une décision explicite.

## 2. Rôles et responsabilités proposés

Le contexte indique un usage initial personnel, mais aucune personne n'est nommée dans les documents comme propriétaire désigné. Les affectations ci-dessous sont donc des rôles à confirmer ; elles ne prétendent pas identifier une personne.

| Rôle | Responsabilité proposée pour le pilote | Affectation / décision |
| --- | --- | --- |
| Propriétaire de plateforme | Décisions globales, configuration des fournisseurs et suspension/révocation d'urgence | Une même personne peut cumuler ce rôle avec propriétaire de projet en pilote personnel ; identité à confirmer |
| Propriétaire de projet | Périmètre, cibles autorisées, finalité, données, permissions et approbations du projet | À confirmer par le propriétaire du dépôt/projet |
| Opérateur | Prépare ou demande une tâche dans le périmètre approuvé ; ne peut pas élargir son autorisation | Pour le pilote personnel, rôle susceptible d'être tenu par le propriétaire de projet ; à confirmer |
| Approbateur | Vérifie séparément les demandes sensibles et les autorisations de cible | Pour les opérations impliquant une cible réelle, privilégier une personne distincte ; si cela n'est pas possible, garder ces opérations bloquées jusqu'à décision explicite |
| Auditeur REA | Documente les constats et sources pour la révision épinglée | À désigner ; audit non effectué |

**Séparation minimale proposée :** une personne ne s'accorde pas silencieusement une autorisation. Toute opération sur une cible réelle nécessite une preuve d'autorisation enregistrée et une approbation séparée, ou reste interdite jusqu'à décision du propriétaire. La faisabilité d'une séparation des rôles en usage personnel reste à arbitrer.

## 3. Référence immuable REA proposée pour l'audit

- Dépôt source : [`morluto/rea`](https://github.com/morluto/rea)
- Branche observée : `main` (branche mutable ; citée uniquement pour le contexte)
- Commit épinglé comme référence candidate : [`3345019fe1341db40c26af3463e136fcb7c7d11e`](https://github.com/morluto/rea/commit/3345019fe1341db40c26af3463e136fcb7c7d11e)
- Date d'observation du commit : 2026-11-10 (métadonnées GitHub)
- Statut : référence immuable candidate à auditer ; l'épinglage ne signifie pas que l'audit, la revue de licence ou la compatibilité ont été vérifiés.
- Étape suivante : le propriétaire confirme que ce commit est la référence retenue ; l'auditeur renseigne les sources, limites et constats dans le plan/rapport d'audit avant toute conclusion sur REA.

Ne pas substituer ultérieurement le contenu courant de `main` à ce SHA. Toute autre révision exige une nouvelle référence et une comparaison/documentation distincte.

## 4. Décisions restant ouvertes et approbation

| Décision | Statut | Responsable |
| --- | --- | --- |
| Accepter le périmètre personnel, les opérations permises et les exclusions ci-dessus | À valider | Propriétaire du projet |
| Confirmer les noms/personnes tenant les rôles et les règles de séparation | À valider | Propriétaire du projet |
| Confirmer le commit REA épinglé comme référence d'audit | À valider | Propriétaire du projet |
| Désigner l'auditeur et autoriser séparément l'examen documentaire de cette révision | Ouvert | Propriétaire du projet |
| Autoriser toute opération ultérieure sur cible réelle | Non accordé | Porte et approbation distinctes requises |

| Visa | État | Validateur / date |
| --- | --- | --- |
| Préparation de cette proposition documentaire | Consignée | Assistant / 2026-11-10 |
| Approbation du périmètre et des rôles | En attente | Propriétaire du projet |
| Confirmation de la référence REA | En attente | Propriétaire du projet |

## 5. Conséquence sur les portes du projet

La proposition de pilote et le commit épinglé ne clôturent pas l'audit REA ni la phase 3. La phase 1 reste incomplète jusqu'à production d'un audit sourcé ; les phases 2 et 3 restent à valider par le propriétaire ; la phase 4 n'est pas franchie. Aucun développement, test sur cible, exécution de REA ou déploiement n'est autorisé par cette décision documentaire.
