# Plan documentaire d'audit de REA

**Statut :** protocole proposé ; l'audit n'a pas été exécuté. Aucun comportement, outil, transport ou prérequis du moteur n'est tenu pour vérifié par ce document.

## Objectif et limites

Produire un rapport reproductible sur une révision précisément identifiée de `morluto/rea`, afin de savoir si et comment une intégration pourrait être conçue. L'audit ne modifie pas le dépôt externe, ne lance pas REA contre une cible réelle, n'installe pas de dépendance et n'autorise pas une analyse de cible. Toute étape nécessitant une exécution ou une installation doit faire l'objet d'une autorisation et d'un plan distincts ; elle est hors du travail documentaire actuel.

## Identité de la révision — à renseigner avant audit

| Champ | Valeur |
| --- | --- |
| URL du dépôt source | `https://github.com/morluto/rea` |
| Tag, commit immuable ou autre identifiant exact | À choisir ; non renseigné |
| Date de consultation | À renseigner |
| Sources consultées (chemins/URL) | À renseigner |
| Auditeur et limites de l'examen | À renseigner |
| Licence et avis associés | À vérifier et citer |

Ne pas agréger les observations de versions différentes. Si la révision change, créer un rapport distinct ou documenter explicitement la comparaison.

## Axes d'examen et preuves attendues

| Axe | Éléments à relever | État actuel |
| --- | --- | --- |
| Interface publique | CLI, API, MCP ou autres interfaces réellement déclarées ; sources et schémas | Non vérifié |
| Transport et cycle de vie | Modes de connexion, lancement, arrêt, annulation et timeouts si documentés | Non vérifié |
| Entrées/sorties | Schémas, erreurs, statuts, résultats partiels et compatibilité | Non vérifié |
| Capacités et providers | Noms exacts, conditions, versions, systèmes et limites observés | Non vérifié |
| Sessions et preuves | Identifiants, persistance, provenance et formats effectivement exposés | Non vérifié |
| Dépendances et installation | Prérequis déclarés, versions, provenance et risques de licence | Non vérifié |
| Compatibilité | Matrice documentée par OS, architecture et versions requises | Non vérifié |
| Sécurité | Permissions nécessaires, accès réseau/fichiers, frontières et contrôles observables | Non vérifié |
| Maintenance | Versions, changements incompatibles et politique de mise à jour si disponibles | Non vérifié |

## Méthode de consignation

Pour chaque constat, consigner : identifiant, statut (`vérifié`, `hypothèse`, `inconnu`, `non applicable`), formulation précise, source et chemin, révision de la source, date de consultation, contexte et limites. Une documentation du dépôt constitue une preuve de ce qui est déclaré, pas nécessairement une preuve d'exécution ou de compatibilité. Une absence de mention est `inconnue`, pas une preuve d'absence.

Ne pas recopier des commandes d'anciennes notes comme procédure validée. Si une commande est découverte lors d'un audit ultérieurement autorisé, la citer avec source/version et indiquer si elle a été seulement documentée ou effectivement vérifiée.

## Livrables de sortie

1. Révision et sources identifiées.
2. Matrice des interfaces, capacités et prérequis, avec statut et preuve par ligne.
3. Analyse des licences, dépendances et limites d'utilisation.
4. Écarts entre les besoins plateforme et les contrats observés.
5. Risques, inconnues, recommandations d'intégration et questions à faire trancher.
6. Conclusion : compatible sous conditions, incompatible ou indéterminé — avec justification et sans extrapolation.

## Porte de clôture

La phase d'audit ne peut être marquée terminée que si la révision est épinglée, les axes pertinents sont sourcés, les inconnues sont explicites, la revue des licences est documentée et le rapport est relu. La clôture de cet audit ne clôt pas la conception ni n'autorise automatiquement le développement.
