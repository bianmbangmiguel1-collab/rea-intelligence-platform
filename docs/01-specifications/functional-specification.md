# Spécification fonctionnelle — version de conception

**Statut :** proposition de conception. Les fonctionnalités dépendant d'un contrat REA sont conditionnelles à l'audit de la révision retenue.

## 1. Acteurs

- **Propriétaire/administrateur :** configure le projet, les agents, les fournisseurs, les budgets et les autorisations.
- **Opérateur :** crée des projets et demande des analyses dans un périmètre qui lui est accordé.
- **Lecteur :** consulte les analyses, preuves et rapports autorisés.
- **Agent d'analyse :** environnement approuvé qui exécute les opérations autorisées.
- **Service externe IA :** reçoit uniquement les éléments explicitement autorisés par la politique de données.

Pour le premier usage personnel, ces rôles peuvent être exercés par une seule personne, sans exclure leur séparation ultérieure.

## 2. Parcours produit

### 2.1 Créer un projet et déclarer une cible

L'utilisateur crée un projet, décrit son objectif, ajoute une ou plusieurs cibles et consigne la provenance, les limites, l'autorisation, la période et les exclusions. Une analyse ne peut pas être planifiée si l'autorisation est absente, expirée ou hors périmètre.

### 2.2 Vérifier les moyens disponibles

La plateforme affiche les agents inscrits, leur état, leur version d'agent/REA et leurs capacités détectées avec la date de découverte. Une capacité expirée ou inconnue ne vaut pas capacité disponible. Si aucun agent ne correspond, l'interface explique les prérequis manquants et n'envoie pas de job.

### 2.3 Demander et suivre une analyse

Avant soumission, l'utilisateur voit le périmètre, le type d'opérations, les données qui peuvent être transférées, l'agent candidat et les approbations requises. Une fois acceptée, l'analyse expose un état, les étapes connues, les journaux filtrés, les erreurs, les résultats et les preuves.

Les états de plateforme proposés sont `draft`, `queued`, `assigned`, `accepted`, `running`, `waiting_for_approval`, `cancelling`, `succeeded`, `failed`, `cancelled` et `interrupted`. Ils ne sont pas attribués à REA.

### 2.4 Examiner les résultats

Chaque observation doit relier sa source, sa date, sa cible, son job, sa session d'exécution, l'outil/version disponibles, les limitations et l'artefact éventuel. Les synthèses et résultats IA sont identifiés comme dérivés et ne remplacent pas la sortie source.

### 2.5 Générer et exporter un rapport

Le rapport présente le périmètre et la méthode, les observations, les hypothèses, les conclusions étayées, les inconnues, les limites et les preuves citées. Un export doit respecter les droits et la classification des données.

## 3. Exigences fonctionnelles

| ID | Exigence |
| --- | --- |
| FR-01 | Créer, modifier, archiver et consulter un projet. |
| FR-02 | Enregistrer cible, provenance, périmètre autorisé, exclusions et échéance. |
| FR-03 | Refuser la création d'un job dont le périmètre est absent ou invalide. |
| FR-04 | Afficher agents, dernière activité, versions et capacités datées. |
| FR-05 | Sélectionner un agent seulement si ses capacités et politiques conviennent au job. |
| FR-06 | Présenter un aperçu des opérations et demander approbation lorsque la catégorie l'exige. |
| FR-07 | Suivre progression, erreurs, état et demande d'annulation. |
| FR-08 | Conserver les résultats sources disponibles ainsi que leur provenance et leurs limites. |
| FR-09 | Relier preuves, cible, étape, session REA, artefacts et conclusions. |
| FR-10 | Produire des rapports distinguant observations, hypothèses, inconnues et conclusions validées. |
| FR-11 | Importer des ressources en quarantaine, inspecter et faire approuver avant activation. |
| FR-12 | Utiliser l'IA uniquement selon une politique de données et de budget configurée. |
| FR-13 | Permettre l'exécution sans IA externe. |
| FR-14 | Journaliser actions privilégiées, attribution des jobs, approbations et transferts de données. |
| FR-15 | Révoquer un agent, un fournisseur ou un accès sans effacer silencieusement les traces historiques. |

## 4. Exigences non fonctionnelles à préciser

- **Sécurité :** moindre privilège, authentification, autorisation par projet, secrets protégés et révocation.
- **Confidentialité :** classification, minimisation, choix des données exportées et politique de rétention/suppression.
- **Intégrité :** empreintes des fichiers et traçabilité des transformations.
- **Robustesse :** idempotence des événements, reprise vérifiée, erreurs compréhensibles et aucun succès inféré après interruption.
- **Observabilité :** logs structurés expurgés, métriques de santé et identifiants de corrélation.
- **Compatibilité :** version REA et inventaire de capacités associés aux exécutions ; incompatibilités explicites.
- **Accessibilité :** interface navigable au clavier et états lisibles sans dépendre uniquement de la couleur.

Les seuils numériques de performance, disponibilité, rétention, taille et délai restent à décider à partir des besoins réels.

## 5. Règles opérationnelles et de sécurité

- Les cibles web doivent être explicitement autorisées et leurs destinations contrôlées contre l'accès non prévu aux réseaux privés.
- Les binaires et archives sont traités comme non fiables, en environnement isolé et avec limites de ressources.
- Aucun script importé n'est exécuté automatiquement.
- Les opérations dynamiques ou susceptibles de modifier une cible requièrent une autorisation explicite ; les opérations destructrices ou de contournement sont hors périmètre.
- Les modèles IA ne peuvent ni approuver leurs propres actions ni modifier les permissions d'exécution.
- Le partage vers OpenRouter ou tout autre service externe doit être visible et contrôlable.

## 6. Critères d'acceptation transversaux

1. Un job sans autorisation valide ne peut pas atteindre un agent.
2. L'interface n'affiche pas une capacité comme disponible sans source, agent et date d'observation.
3. Une interruption ou erreur reste distincte d'une réussite.
4. Un rapport permet de naviguer de toute conclusion vers ses preuves sources.
5. La désactivation de l'IA ne bloque pas la conservation des résultats techniques.
6. Un import en quarantaine n'est ni exécuté ni mis à disposition avant approbation.
7. Les paramètres et événements de chaque job permettent d'expliquer qui a demandé, approuvé, exécuté et reçu les données.

## 7. Dépendances à l'audit REA

La découverte des outils, les formats de sortie, les sessions, l'annulation, les Evidence et les conditions par système doivent être confirmés sur une révision déterminée de REA. Jusqu'à cette validation, les exigences FR-04, FR-05, FR-07 et FR-08 décrivent le comportement souhaité de la plateforme et non des garanties fournies par REA.