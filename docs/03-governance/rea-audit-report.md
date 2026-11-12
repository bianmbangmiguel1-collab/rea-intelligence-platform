# Rapport d'audit documentaire REA — révision de référence

**Statut :** audit documentaire des sources publiques épinglées ; ce n'est ni une exécution de REA, ni un audit de sécurité indépendant, ni une validation de compatibilité opérationnelle. La matrice distingue les constats sourcés des questions restant ouvertes.

## 1. Identité, portée et méthode

- Dépôt source : [`morluto/rea`](https://github.com/morluto/rea)
- Révision étudiée : [`0909d89c966c30955fd0906b622ff25f3700789f`](https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f)
- Date du commit : 2026-11-11T15:49:30Z (métadonnées GitHub consultées pour cette révision)
- Méthode : lecture des fichiers source/documentation de cette révision via GitHub ; aucune installation, aucun lancement de REA, aucun appel d'outil REA et aucune analyse de cible n'ont été faits.
- Limite : la revue porte sur les sources documentaires listées ci-dessous ; la totalité du catalogue d'outils généré, des implémentations de tous les providers, des dépendances transitoires et des comportements à l'exécution n'a pas été auditée.
- Conclusion : **contrat partiellement documenté, intégration plateforme non encore approuvée ni validée**. La révision peut servir de référence pour une analyse plus ciblée, mais ce rapport seul ne satisfait pas tous les critères de clôture d'audit opérationnel.

## 2. Sources primaires consultées

Tous les liens de cette table sont épinglés sur la même révision.

| Source | Faits étayés par cette source |
| --- | --- |
| [`README.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/README.md) | Positionnement, utilisation locale, exigences runtime publiées, grandes familles d'analyses, caractère statique ou dynamique signalé, limites de compatibilité selon workflows et avertissements d'usage. |
| [`package.json`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/package.json) | Nom/version `rea-agents` `6.8.0`, type module, exécutables CLI, moteurs Node déclarés, scripts et dépendances directes déclarées. Ce fichier ne prouve pas qu'une installation ou un test a été exécuté ici. |
| [`server.json`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/server.json) | Métadonnées d'enregistrement MCP : package npm `rea-agents` `6.8.0`, lancement par `npx`, argument `mcp`, transport `stdio`. Cela ne décrit pas l'ensemble des outils et de leurs schémas. |
| [`mcp.json`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/mcp.json) | Exemple de configuration d'un serveur MCP local via `npx` et stdio, avec version publiée 6.8.0. Exemple documentaire, non exécuté. |
| [`docs/reference/mcp-contracts.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/docs/reference/mcp-contracts.md) | Contrats de transport, résultats, Evidence conservées, erreurs, délais/capacité de réponse et règles de reprise décrits dans la référence MCP. Le catalogue complet des outils est un artefact distinct à extraire/revoir avant intégration précise. |
| [`docs/getting-started/cli.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/docs/getting-started/cli.md) | Contrats CLI/Evidence et exemples de workflows ; sortie JSON/JSONL, limites et distinction entre sortie complète et export partiel. Les exemples ne constituent pas une autorisation d'opérer sur une cible. |
| [`docs/getting-started/installation.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/docs/getting-started/installation.md) | Procédure et portée de configuration, approbation de changements, diagnostics en lecture seule et limites de séparation entre profils. Les commandes d'installation ne sont pas exécutées ni recommandées par ce rapport. |
| [`SECURITY.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/SECURITY.md) | Frontière de sécurité, droits de l'utilisateur hôte, risques liés aux providers, limites de sandbox, transports, données et ressources. |
| [`DISCLAIMER.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/DISCLAIMER.md) | Usage autorisé, responsabilité de l'utilisateur, distinction entre inspection d'artefact et exécution/interactions, limites des résultats et droits sur les outils tiers. |
| [`LICENSE`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f3700789f/LICENSE) et [`THIRD_PARTY_NOTICES.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f/THIRD_PARTY_NOTICES.md) | Licence MIT du code REA-authored et inventaire/avertissements sur les licences tierces. Le MIT de REA ne donne aucun droit sur les outils propriétaires ou les dépendances externes. |
| [`docs/guides/native/native-initializers.md`](https://github.com/morluto/rea/blob/0909d89c966c30955fd0906b622ff25f/docs/guides/native/native-initializers.md) et le [commit source](https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f) | Changement associé au commit sélectionné concernant les initialisateurs et relocations natifs ; ce changement isolé ne prouve pas la compatibilité générale ni la couverture de l'application. |

## 3. Matrice d'audit

Statuts : **vérifié documentairement** = énoncé explicitement par une source épinglée ; **partiel** = source utile mais couverture incomplète ; **inconnu** = aucune preuve consultée suffisante ; **non testé** = aucune exécution réalisée.

| ID | Domaine | Constat documentaire | Preuve / révision | Statut et conséquence d'intégration |
| --- | --- | --- | --- | --- |
| A-01 | Identité du paquet | Le paquet se nomme `rea-agents`, version 6.8.0 ; le manifeste déclare des binaires CLI `rea` et `rea-agents`. | `package.json`, même commit | Vérifié documentairement ; publication exacte et provenance de l'artefact à vérifier avant distribution. |
| A-02 | Runtime | `package.json` déclare Node `^22.23.4 || ^24.22.1 || >=26.12.1`, npm 11.16.0 comme package manager. | `package.json` | Vérifié documentairement ; test Windows/Linux/macOS et disponibilité runtime non réalisés. |
| A-03 | Interface locale | Le dépôt documente CLI et serveur MCP ; exemple MCP déclare `stdio`, package 6.8.0, lancement `npx ... mcp`. | `server.json`, `mcp.json`, README | Vérifié documentairement pour le mode indiqué ; aucun serveur lancé ici. |
| A-04 | Interface HTTP | La politique sécurité indique qu'un transport MCP HTTP opt-in est plain HTTP sans TLS ni authentification client et partage l'état provider/cible active entre sessions. | `SECURITY.md` et référence MCP | Vérifié documentairement ; ne pas exposer ce transport au backend/cloud. Pour une intégration initiale, ne retenir que stdio local si l'interface et le contrat exacts sont ensuite validés. |
| A-05 | Catalogue d'outils | La documentation MCP renvoie au catalogue généré et à `tools/list`; cet audit n'a pas extrait ni vérifié toutes les entrées, schémas, descriptions, effets et providers disponibles. | Référence MCP | Partiel ; bloquant pour tout mapping de contrat ou appel d'outil non documenté dans une fiche propre à l'opération. |
| A-06 | Entrées/sorties | La référence décrit `structuredContent.normalized_result`, `evidence_id`, `raw_result` optionnel, enveloppes d'erreur, statuts de couverture et Evidence retenue. La sémantique dépend du producteur et du workflow. | Référence MCP, CLI | Vérifié documentairement au niveau des règles communes ; schémas par outil et compatibilité de notre modèle non établis. |
| A-07 | Erreurs et résultats partiels | La référence décrit erreurs explicites, champs de récupération possibles, limites de transport et que pages/résultats partiels ne prouvent pas la complétude. Une interruption ne doit pas être interprétée comme réussite. | Référence MCP, CLI | Vérifié documentairement ; tests d'intégration de notre consommateur non réalisés. |
| A-08 | Evidence et sessions | Evidence porte identité, provenance et liens ; résultats retenus dans la session, exports de bundles et vues paginées sont décrits. La persistance n'est pas assimilable à une base durable de notre plateforme. | Référence MCP | Partiel à vérifié selon les mécanismes décrits ; schéma d'archivage, rétention et récupération côté plateforme à concevoir. |
| A-09 | Annulation / reprise | La référence contient un chapitre de progression/annulation et décrit des erreurs/états de récupération spécifiques ; les garanties sont propres à l'opération/provider. | Référence MCP | Partiel ; ne pas promettre un arrêt ferme. Inconnu pour chaque opération non examinée. |
| A-10 | Effets et frontière de sécurité | REA s'exécute avec les permissions du processus hôte ; ce n'est ni une sandbox générale ni un service d'autorisation multi-tenant. Certaines workflows peuvent exécuter du code, ouvrir des processus, agir sur fichiers, réseau, applications ou appareils. | `SECURITY.md` | Vérifié documentairement ; intégration côté serveur multi-tenant et accès réseau distant ne sont pas acceptables sans isolation et contrôle externes démontrés. |
| A-11 | Chemins d'intégration conservateurs | La documentation distingue des inspections statiques qui ne lancent pas l'application cible de workflows dynamiques/runtime qui peuvent l'exécuter ou interagir avec elle. | README, SECURITY, DISCLAIMER | Vérifié documentairement comme distinction ; le périmètre du pilote doit exclure les workflows dynamiques jusqu'à décision, autorisation et validation séparées. |
| A-12 | Réseau HTTP/MCP | La documentation avertit des interactions navigateur/réseau et des endpoints HTTP MCP sans authentification/TLS ; une cible et ses redirections peuvent exposer des réseaux inattendus. | SECURITY, README, référence MCP | Vérifié comme risque ; aucune analyse de cible web ni accès réseau autorisé par ce rapport. |
| A-13 | Providers et OS | README donne des exigences variées par workflow ; certains providers requièrent logiciels tiers, runtimes et OS précis. L'existence d'une entrée n'est pas preuve de disponibilité universelle. | README, installation, package | Partiel ; matrice d'OS à remplir pour chaque workflow retenu, aucune compatibilité Windows de l'agent REA n'est inférée. |
| A-14 | Dépendances/licences | Code REA-authored annoncé MIT ; `THIRD_PARTY_NOTICES.md` précise les dépendances, composants dérivés, outils séparés et outils commerciaux sous contrats distincts. | LICENSE, THIRD_PARTY_NOTICES, package-lock | Partiel ; revue juridique complète de toutes les dépendances/transitives et des conditions d'usage du pilote non réalisée. |
| A-15 | Résultats / confiance | Le disclaimer prévient que décompilation, reconstruction, heuristiques et IA peuvent être incomplets/incorrects et que l'Evidence doit être revue. | DISCLAIMER | Vérifié ; la plateforme doit conserver limites/inconnues et ne pas présenter une analyse comme vérité ou preuve d'autorisation. |
| A-16 | Installation / mutation locale | `rea setup` affiche les changements et sollicite une approbation ; cette fonctionnalité modifie configurations et peut installer des outils si autorisée. | `docs/getting-started/installation.md`, SECURITY | Vérifié documentairement ; installation/setup hors périmètre de cet audit. |
| A-17 | Tests d'exécution | Aucun test, lancement, vérification de paquet ni test sur cible n'a été exécuté dans le cadre de ce rapport. | Journal de cette revue | Non testé ; ne pas transformer les constats documentaires en assurance de sécurité ou de compatibilité. |

## 4. Périmètre d'intégration proposé — non approuvé

Pour réduire le risque du premier prototype, proposer une frontière limitée à :
- processus REA local via l'interface documentée, transport stdio uniquement après vérification des arguments et réponses exacts de la révision ;
- artefacts synthétiques ou appartenant au projet et explicitement autorisés ;
- workflows statiques précis dont l'absence d'exécution de la cible est documentée ;
- un seul utilisateur/opérateur local dans un environnement contrôlé ;
- aucun endpoint HTTP MCP distant, aucun workflow dynamique/runtime, aucun réseau cible, aucun appareil, aucun outil propriétaire sans licence, aucun fournisseur IA.

Cette proposition ne vaut pas décision du propriétaire, autorisation de lancer REA ni autorisation d'analyser un fichier réel. Avant mapping d'un outil, ajouter son nom exact, sa source de catalogue, son schéma d'entrée/sortie, ses prérequis, effets, limites et tests.

## 5. Questions bloquantes restantes

1. Extraire et figer le catalogue complet `tools/list` (ou l'artefact catalogue canonique) pour cette révision, puis sélectionner seulement les opérations nécessaires au pilote.
2. Pour chaque outil retenu, citer la source d'implémentation et de contrat, les champs/erreurs, les effets de provider, les limites, la sémantique partielle et l'annulation.
3. Vérifier de façon documentée la build/package distribuée correspondant au SHA et les versions de dépendances effectivement livrées.
4. Décider du pilote, des rôles, du runtime, de l'OS et du modèle d'isolation ; les documents de conception actuels laissent plusieurs arbitrages ouverts.
5. Réconcilier `AGENTS.md` : il interdit encore le code applicatif, l'installation, l'exécution de REA, les analyses réelles et le déploiement. Ce rapport ne lève pas cette interdiction.
6. Obtenir une autorisation écrite spécifique avant tout test d'exécution, même sur artefact synthétique si cela nécessite lancement d'outils/installation, et distincte avant toute cible réelle.

## 6. Décision d'audit

**Résultat : révision identifiée et sources de haut niveau consultées ; audit des contrats et validation technique incomplets.** Ce document remplace toute affirmation antérieure selon laquelle le seul SHA aurait clos à lui seul l'audit REA. La clôture de la phase 1 et l'ouverture technique de la phase 5 exigent la résolution des questions bloquantes et l'approbation propriétaire selon les règles du dépôt.
