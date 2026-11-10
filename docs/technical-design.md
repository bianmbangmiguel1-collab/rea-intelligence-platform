# Cahier d'architecture et de conception

> Statut : conception fonctionnelle et technique en cours. Aucun code applicatif n'est ajouté à cette étape.

Le document est une vue d'ensemble conceptuelle ; les exigences et détails complémentaires sont répartis dans les documents spécialisés.

## 1. Objet

Construire une plateforme indépendante autour du moteur officiel REA (`morluto/rea`), sans réécrire le moteur ni en faire un fork principal. La plateforme fournit interface, projets, cibles, orchestrateur, agents, preuves, IA facultative, rapports et audit.

## 2. Principes

- REA est le moteur technique ; la plateforme l'intègre et le gouverne.
- Les interfaces et capacités réelles de REA sont à vérifier dans une révision épinglée.
- L'agent exécute les opérations qui nécessitent l'environnement local ou des outils natifs.
- L'IA aide à planifier/interpréter/rédiger ; elle n'autorise pas de commandes.
- Les preuves sources, erreurs et limites restent distinctes des synthèses.
- Aucune cible n'est traitée sans autorisation et périmètre.
- Aucun code n'est commencé avant validation explicite de la conception.

## 3. Architecture générale proposée

Navigateur web → application → backend modulaire → orchestrateur et registre d'agents → agent local ou runner → REA par les interfaces confirmées. Le backend conserve les métadonnées et événements ; stockage objet privé candidat pour les artefacts volumineux. Le routeur IA est facultatif et séparé du chemin d'exécution technique.

## 4. Responsabilités principales

- **Web :** projets, cibles, workspace d'analyse, preuves, rapports, agents et paramètres.
- **Backend :** identité, autorisation, projets, orchestration, registre des agents, adaptateurs, audit et reporting.
- **Agent :** découverte locale, validation de tâche, lancement REA autorisé, remontée de diagnostics et artefacts.
- **REA :** opérations techniques effectivement prises en charge par la version et les providers installés.
- **Routeur IA :** filtrage et sélection de modèles selon capacité, données, budget et disponibilité.

## 5. Flux principal

1. Enregistrer projet, cible, provenance et autorisation.
2. Valider le périmètre et les approbations.
3. Comparer les exigences au catalogue d'agents et à la fraîcheur de leurs capacités.
4. Attribuer une tâche à un agent identifié et compatible.
5. Exécuter uniquement l'opération correspondant au contrat REA vérifié.
6. Préserver résultats, erreurs, limites, références et artefacts.
7. Analyser éventuellement un extrait minimisé avec un modèle autorisé.
8. Générer un rapport référencé et conserver l'audit.

## 6. Preuves et résultats

Une preuve est conservée avec source, type, date, contexte cible/projet/job, outil/version disponibles, statut de complétude, limites et référence d'artefact. Les catégories internes de présentation sont : observé, dérivé, hypothèse, inconnu, validé. La forme exacte des Evidence REA reste à auditer.

## 7. Sécurité

Quarantaine des imports, aucune exécution automatique, environnement isolé, limites de ressources, autorisation par cible, restrictions réseau, agent révocable, secrets protégés, journaux expurgés et contrôle explicite des transferts vers IA externe. Les détails sont dans [la conception sécurité](02-architecture/security-design.md).

## 8. Documents associés

- [Spécifications fonctionnelles](01-specifications/functional-specification.md)
- [Architecture détaillée](02-architecture/detailed-architecture.md)
- [Sécurité et modèle de menace](02-architecture/security-design.md)
- [Modèle de données](04-data-model/data-model.md)
- [Contrats API proposés](05-api-contracts/api-contracts.md)
- [Roadmap](06-roadmap/roadmap.md)
- [Décisions d'architecture](07-decisions/README.md)

## 9. Limite actuelle

L'audit officiel REA n'étant pas clôturé, les commandes, transports, schémas, formats, sessions, Evidence, providers et prérequis mentionnés dans les anciennes notes doivent être considérés comme des hypothèses à valider. Aucun test ou analyse réelle n'est déclaré effectué.