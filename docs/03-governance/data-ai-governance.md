# Gouvernance des données et de l'IA

**Statut :** principes proposés ; aucune région, durée, fournisseur, configuration contractuelle ou transfert de données n'est validé.

## Objectifs

Limiter les données aux besoins du projet, rendre visibles les flux, préserver la provenance et permettre l'usage sans IA distante. Les exigences ci-dessous doivent être converties en décisions vérifiables avant réalisation.

## Classification proposée

| Classe | Exemples conceptuels | Règle proposée |
| --- | --- | --- |
| Public | Informations destinées à être publiées | Partage possible selon droits et licence |
| Interne | Configuration et métadonnées ordinaires du projet | Accès authentifié et limité au projet |
| Confidentiel | Sources privées, preuves, résultats non publiés | Accès minimal ; pas de fournisseur externe par défaut |
| Secret | Identifiants, jetons, clés, données d'authentification | Ne jamais inscrire dans prompt, log, rapport ou artefact exporté |

Le propriétaire du projet doit pouvoir classer les données et définir les catégories interdites au transfert. La classification n'est pas une garantie de sécurité par elle-même.

## Principes de traitement

1. Ne collecter et conserver que ce qui est nécessaire à une finalité documentée.
2. Séparer contenu source, dérivés, synthèses IA et décisions humaines.
3. Relier chaque dérivé aux données sources utilisées, au traitement et à la version disponibles.
4. Refuser un transfert externe si la politique, le consentement, le fournisseur ou la destination ne sont pas explicitement définis.
5. Permettre un mode sans IA qui conserve les résultats techniques et leurs preuves.
6. Définir avant réalisation les accès, région, chiffrement, durées, suppression, sauvegarde et obligations applicables.

## Gouvernance des appels IA — proposition

Avant un appel, montrer l'objectif, le fournisseur/modèle envisagé, les preuves ou extraits transmis, leur classification, les transformations, le coût estimé si disponible, la politique de rétention connue et l'approbation requise. Minimiser et expurger les données ; conserver un journal d'audit de la décision sans y recopier les secrets.

L'IA peut aider à résumer, classer ou rédiger des hypothèses si le cas d'usage est accepté. Elle ne décide pas seule du périmètre, n'autorise pas une action, ne déclenche pas d'exécution et ne transforme pas une hypothèse en fait. Les résultats d'IA doivent être identifiés et reliés aux sources disponibles.

OpenRouter reste un fournisseur envisagé, pas un choix accepté : les modèles accessibles, routage, conditions, traitement, rétention, région et garanties doivent être examinés au moment de la décision. Ne pas présumer que le routage via un fournisseur implique une protection particulière.

## Décisions à obtenir

- Catégories autorisées/interdites par fournisseur et finalité.
- Consentement par projet ou par appel, et personnes habilitées à l'accorder.
- Fournisseurs/modèles approuvés, conditions contractuelles et contrôles applicables.
- Rétention côté plateforme et prestataires, localisation et suppression.
- Seuils de coût, traitement des erreurs et comportement si le fournisseur est indisponible.
- Processus d'accès, export, rectification et suppression selon les obligations applicables.

## Critère de passage

Aucun flux de données externe ne peut être considéré prêt à réaliser tant que les données transmises, la base d'autorisation, le fournisseur, les paramètres de confidentialité, la rétention, l'accès et les critères de désactivation ne sont pas définis et validés.
