# Plan de travail et backlog initial — phase 5

**Statut :** plan de travail documentaire **validé par le propriétaire le 2026-11-12** pour guider le sous-périmètre restreint. Cette validation porte sur le plan, **pas sur la réalisation ni sur la clôture de la phase 5**. Aucun des travaux ci-dessous n'est marqué comme réalisé par la création ou l'approbation de ce document. La phase 5 reste ouverte et non validée.

## 1. Périmètre de référence

Suivre l'autorisation de [`implementation-authorization.md`](implementation-authorization.md) et les restrictions de [`AGENTS.md`](../../AGENTS.md) : prototype local mono-utilisateur, pas de production, pas de nouvelles dépendances/outils, pas d'exécution ou d'installation REA, pas de cible réelle, pas de transfert externe et pas de déploiement.

Les tâches de ce plan doivent être réalisées avec les outils déjà disponibles et des données/fixtures synthétiques. Si une tâche nécessite une capacité interdite ou une nouvelle décision technique, la marquer **bloquée** et demander une autorisation distincte avant d'agir.

## 2. Séquence de travail

### Lot 0 — Vérifier l'espace de travail et les limites

- [ ] Confirmer que le travail se fait dans le dépôt et la branche de travail prévus.
- [ ] Relire l'autorisation et vérifier qu'aucune nouvelle dépendance n'est requise.
- [ ] Confirmer qu'aucune commande de test ne lance REA, un provider ou un accès réseau.
- [ ] Utiliser exclusivement des données synthétiques ; ne pas inclure de secrets ou de fichiers d'analyse.

**Sortie :** note de périmètre de la tâche et préconditions vérifiées. Si une précondition échoue, arrêter et consigner le blocage.

### Lot 1 — Contrats de domaine et états

- [ ] Définir les types conceptuels minimaux : projet, cible déclarée (métadonnées synthétiques seulement), autorisation, tâche, événement de tâche, preuve et observation.
- [ ] Formaliser des états de plateforme et les transitions permises, sans les confondre avec des états REA.
- [ ] Définir les champs obligatoires de provenance : acteur, projet, tâche, horodatage, source/version, statut de couverture et limitations.
- [ ] Définir des erreurs/états distincts : refus, échec, interruption, résultat partiel et succès vérifié.

**Sortie :** contrat de domaine documenté ou types purs sans dépendance, plus critères de vérification associés.

### Lot 2 — Validation d'autorisation et de périmètre, sans moteur

- [ ] Modéliser l'autorisation comme donnée explicite et bornée (projet, action déclarative, portée, exclusions et échéance).
- [ ] Définir le refus par défaut pour permission absente, expirée, contradictoire ou hors périmètre.
- [ ] Séparer les décisions d'autorisation des données de cible, des fixtures et de tout contenu non fiable.
- [ ] Construire une interface d'exécution abstraite qui ne lance aucun processus et dont le faux adaptateur peut seulement retourner des résultats prédéterminés.

**Sortie :** logique pure testable ; aucune commande, connexion ou intégration REA.

### Lot 3 — Traçabilité et traitement de résultats synthétiques

- [ ] Relier les événements simulés à une tâche et conserver ordre, erreurs, limitations et résultat partiel.
- [ ] Ajouter des empreintes aux fixtures synthétiques lorsque l'intégrité est pertinente ; ne jamais déduire qu'une empreinte prouve l'autorisation ou la sécurité.
- [ ] Produire un rapport synthétique distinguant observation, hypothèse, inconnu et conclusion dérivée.
- [ ] S'assurer que le mode sans IA est le seul mode du prototype autorisé pour ce lot.

**Sortie :** scénario bout en bout synthétique, sans cible réelle ni appel externe.

### Lot 4 — Vérifications locales autorisées

Sélectionner dans le [protocole de recette](phase-5-acceptance-protocol.md) les scénarios compatibles avec les interdictions du dépôt, notamment :
- [ ] refus de permission absente/expirée avec adaptateur simulé jamais appelé ;
- [ ] refus d'une action inconnue ou d'un périmètre hors allowlist ;
- [ ] absence de succès lors d'une erreur ou interruption simulée ;
- [ ] conservation de provenance et limitations dans les résultats synthétiques ;
- [ ] aucun canari de secret synthétique dans les sorties/journaux produits ;
- [ ] aucun accès réseau ni lancement de processus dans le parcours testé.

Ne pas exécuter de test qui installe un outil, lance REA/provider, contacte un service, lit une cible réelle ou dépasse les permissions du workspace.

### Lot 5 — Revue de livraison

- [ ] Consigner commit, tests réellement exécutés, résultats détaillés et échecs.
- [ ] Comparer les preuves aux critères et noter les cas non exécutés comme tels.
- [ ] Lister défauts et risques résiduels avec propriétaire et décision attendue.
- [ ] Demander au propriétaire de revoir les preuves et d'inscrire une décision de recette.
- [ ] Ne demander la clôture qu'après satisfaction des critères requis de phase 5.

## 3. Backlog ordonné

| ID | Tâche | Priorité | Dépendances | État initial |
| --- | --- | --- | --- | --- |
| P5-T01 | Définir les contrats purs projet/tâche/autorisation/preuve | P0 | Aucune | À faire |
| P5-T02 | Documenter états/transitions et états d'erreur/partiels | P0 | P5-T01 | À faire |
| P5-T03 | Concevoir la validation fail-closed du périmètre | P0 | P5-T01 | À faire |
| P5-T04 | Définir une interface d'exécution abstraite sans processus et faux adaptateur déterministe | P0 | P5-T03 | À faire |
| P5-T05 | Préparer fixtures synthétiques et scénario de provenance | P1 | P5-T01, P5-T02 | À faire |
| P5-T06 | Produire rapport synthétique distinguant faits/unknowns/limites | P1 | P5-T05 | À faire |
| P5-T07 | Exécuter les tests locaux permis du protocole et enregistrer les résultats | P1 | P5-T03 à P5-T06 | À faire |
| P5-T08 | Revue des preuves, défauts résiduels et visa de recette propriétaire | P0 clôture | P5-T07 | Bloqué jusqu'aux preuves |

## 4. Checklist des livrables pour clôture

Cette checklist est un suivi ; ne cocher que lorsque la preuve correspondante est présente et consultable.

- [ ] Code/livrables de fondation présents dans un commit identifiable et conformes à l'autorisation.
- [ ] Contrats/types et transitions de tâches documentés et testés.
- [ ] Validation d'autorisation fail-closed démontrée avec cas acceptés et refusés.
- [ ] Faux adaptateur démontré comme ne lançant ni REA ni processus externe.
- [ ] Parcours synthétique préserve provenance, erreurs, interruptions, couverture et limitations.
- [ ] Tests locaux exécutés ; commande/outils, environnement, commit, résultats et artefacts expurgés consignés.
- [ ] Vérification d'absence de secrets et d'accès réseau/processus incluse dans les tests qui s'y prêtent.
- [ ] Anomalies bloquantes absentes ou corrigées ; risques restants associés à un propriétaire et une décision.
- [ ] Protocole et documents de statut mis à jour avec ce qui est réellement vérifié.
- [ ] Validation finale du propriétaire enregistrée après examen des preuves.

## 5. Conditions qui bloquent une tâche ou la phase

Arrêter et documenter le blocage si :
- une dépendance/tooling doit être installé ou téléchargé ;
- un test démarre REA, un provider, un processus cible ou un réseau ;
- les données ne sont pas synthétiques ou leur provenance/autorisation est inconnue ;
- un résultat partiel risque d'être traité comme complet ;
- un secret ou contenu sensible apparaît dans une preuve ;
- une évolution exige de modifier le périmètre approuvé.

Les extensions vers intégration REA, analyse réelle, IA externe, nouvelles dépendances ou déploiement exigent une revue et une autorisation séparées conformément à la porte de phase 4.
