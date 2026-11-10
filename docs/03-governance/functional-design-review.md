# Revue documentaire fonctionnelle — phase 2

**Statut :** revue de cohérence documentaire effectuée ; validation du propriétaire **en attente**. Cette revue n'est ni une recette, ni une validation utilisateur, ni une preuve d'implémentation. Aucune exécution, installation, analyse de cible ou vérification REA n'a été effectuée.

## Portée et méthode

Documents examinés : charte, spécification fonctionnelle, architecture détaillée, modèle conceptuel, contrats API proposés, gouvernance des données/IA, registre des risques, roadmap et contexte projet. La revue vérifie la cohérence interne, la traçabilité et la visibilité des points bloquants. Elle n'établit pas la faisabilité technique ni la compatibilité avec REA.

## Résultat synthétique

La base fonctionnelle est cohérente au niveau conceptuel : parcours de projet/cible, contrôle d'autorisation, attribution conditionnelle, traçabilité des résultats, rapport et IA facultative sont représentés. La spécification ne peut pas être déclarée finalisée pour réalisation : le périmètre pilote, les priorités, les seuils non fonctionnels, les règles précises d'approbation et le contrat REA restent ouverts. La validation du propriétaire est requise.

## Revue des exigences

| ID | Besoin | Couverture documentaire | Conclusion de revue |
| --- | --- | --- | --- |
| FR-01 | Gérer les projets | Spécification, architecture et modèle de données | Couvert conceptuellement ; droits, archivage et cycle de vie à préciser. |
| FR-02 | Décrire cible, provenance, périmètre, exclusions et échéance | Spécification, modèle et contrats API | Couvert ; formats/preuves et validation du périmètre à détailler. |
| FR-03 | Bloquer un job sans autorisation valide | Spécification et flux d'attribution | Exigence claire ; règles de décision et critères de test à définir. |
| FR-04 | Afficher agents, versions, capacités datées | Spécification, architecture, modèle | Couvert ; distinction déclarée/vérifiée et fraîcheur à préciser. |
| FR-05 | Attribuer selon capacités et politiques | Architecture et spécification | Couvert conceptuellement ; dépend des capacités réellement auditées REA et du modèle agent. |
| FR-06 | Montrer opérations et obtenir approbation | Spécification et contrats API | Partiel ; catégories sensibles, approbateur et règle de séparation des rôles restent à décider. |
| FR-07 | Suivre état, erreurs et annulation | États proposés et événements API | Partiel ; sémantique des transitions, délais et preuve d'arrêt à définir, REA à auditer. |
| FR-08 | Préserver sorties source, provenance et limites | Spécification, modèle et architecture | Couvert comme invariant ; formats et fidélité de la source dépendent de l'audit REA. |
| FR-09 | Relier preuve, cible, étape, session et artefact | Modèle de données et architecture | Couvert conceptuellement ; disponibilité des identifiants/sessions REA non vérifiée. |
| FR-10 | Rapports séparant observations, hypothèses et conclusions | Spécification et modèle | Couvert ; modèle de revue humaine et format de rapport à définir. |
| FR-11 | Quarantaine et approbation des imports | Spécification et sécurité | Exigence claire ; traitement, limites et responsabilité de l'inspection à détailler. |
| FR-12 | IA selon politique et budget | Spécification et gouvernance IA | Couvert en principe ; fournisseur, consentement, données, limites et rétention ouverts. |
| FR-13 | Fonctionner sans IA externe | Spécification et gouvernance IA | Exigence claire ; devra être vérifiée par scénario dédié après autorisation de réalisation. |
| FR-14 | Journaliser actions privilégiées et transferts | Spécification et conception sécurité/exploitation | Couvert conceptuellement ; schéma d'événements, accès et conservation à décider. |
| FR-15 | Révoquer accès, agent ou fournisseur | Spécification et conception sécurité/exploitation | Couvert conceptuellement ; protocole, délais, tâches en cours et preuve d'effet à préciser. |

## Points fonctionnels bloquants avant la porte de réalisation

1. Définir le pilote minimal : utilisateurs, cas d'usage, types de cibles et opérations permises/interdites.
2. Définir la politique d'autorisation et d'approbation, notamment les actions sensibles et l'indépendance de l'approbateur.
3. Fixer les règles de cycle de vie des états, annulation, résultats partiels, reprise et réconciliation après interruption.
4. Définir les objectifs mesurables : performance, disponibilité, quotas, tailles, délais, accessibilité et budgets.
5. Définir les exigences de rapport, revue humaine, export et conservation.
6. Auditer une révision immuable de REA et remplacer les hypothèses d'intégration par des faits sourcés ou des inconnues explicites.
7. Consigner les décisions et arbitrages du propriétaire dans le document de revue de phase ; ne pas déduire une acceptation d'une proposition.

## Critère de validation fonctionnelle proposé

Le propriétaire peut valider la conception fonctionnelle lorsque le périmètre pilote et les rôles sont définis, chaque FR possède un critère d'acceptation et une méthode de vérification, les dépendances REA sont reliées au rapport d'audit, et les inconnues/risques bloquants sont acceptés ou traités explicitement. Les tests fonctionnels restent à exécuter ultérieurement dans un environnement contrôlé et autorisé ; aucun test n'est déclaré réussi ici.

## Décision de revue

**Avis documentaire : favorable sous réserves pour poursuivre la conception ; non prête pour réalisation.** La conception fonctionnelle est suffisamment structurée pour la revue du propriétaire, mais sa validation formelle reste attendue et la dépendance REA demeure ouverte.

| Validation | État | Validateur / date |
| --- | --- | --- |
| Cohérence documentaire interne | Revue effectuée dans le cadre de cette tâche | Assistant / 2026-11-10 |
| Validation fonctionnelle du propriétaire | En attente | À renseigner par le propriétaire |
| Vérification d'implémentation ou recette | Non effectuée | Hors portée de cette revue |
