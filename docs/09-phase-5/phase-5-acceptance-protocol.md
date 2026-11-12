# Protocole de recette fiable — phase 5

**Statut :** protocole proposé ; aucun test de la plateforme n'est affirmé exécuté. Les cas exigent d'abord une autorisation écrite conforme au dépôt et un environnement de test contrôlé.

## Principes de preuve

- Chaque essai porte un ID, une exigence/risque lié, une version de code, un environnement, un opérateur, une date UTC, un résultat attendu, un résultat observé et des artefacts expurgés.
- Utiliser des données synthétiques et une cible locale de test uniquement après autorisation ; pas de système tiers, production, réseau réel ou données personnelles par défaut.
- Préserver les logs et sorties utiles, mais expurger tokens, secrets, contenus sensibles et chemins privés. Ne pas publier de preuves contenant des données de cible.
- Un test non exécuté vaut `non exécuté`, pas `pass`. Un résultat indéterminé ou partiel n'est pas un succès.
- Les tests REA emploient uniquement des opérations précises dont le contrat, l'effet et la révision ont été audités et approuvés ; sinon, remplacer par un faux adaptateur déterministe.
- Exécuter uniquement dans un environnement isolé approuvé, avec limites ressources, accès réseau minimal et procédure d'arrêt. Aucun test de pénétration ni scénario d'exploitation n'est implicite.

## En-tête obligatoire d'un rapport de test

| Champ | Valeur |
| --- | --- |
| Test ID / exigences / risque | À compléter |
| Commit de la plateforme et commit REA | À compléter ; REA attendu `0909d89c966c30955fd0906b622ff25f3700789f` si approuvé |
| Environnement / OS / runtime | À compléter |
| Autorisation et périmètre | Référence écrite à joindre |
| Données de test / provenance | Synthétiques ou autorisées ; préciser |
| Étapes reproductibles approuvées | À consigner sans secret |
| Résultat attendu / observé | À compléter |
| Verdict | `pass / fail / blocked / inconclusive / not run` |
| Logs et preuve expurgés | Références, empreintes et classification |
| Défauts / risques résiduels / approbateur | À compléter |

## Matrice de recette proposée

| ID | Domaine | Précondition / scénario contrôlé | Critère de réussite | Preuve exigée |
| --- | --- | --- | --- | --- |
| P5-F01 | Autorisation | Soumettre une tâche sans permission, permission expirée ou périmètre invalide dans le harness de test. | Rejet avant attribution et avant tout appel à l'adaptateur ; motif traçable, aucun effet externe. | Trace corrélée + assertion du faux adaptateur non appelé. |
| P5-F02 | Isolation projet | Identité A tente de lire/modifier une ressource synthétique du projet B. | Refus côté service pour chaque opération pertinente ; aucune fuite de contenu. | Résultats tests d'accès croisé, sans données réelles. |
| P5-F03 | Allowlist d'actions | Soumettre action inconnue, champ supplémentaire, commande ou destination non prévue. | Validation de schéma fermée ; refus sûr et aucune exécution dynamique/arbitraire. | Tests unitaires négatifs + compteur d'invocations nul. |
| P5-F04 | Échéance et rejeu | Tâche expirée, déjà consommée ou répétée injectée dans un simulateur. | Agent/service refuse l'exécution répétée ou périmée ; état et cause ne sont pas présentés comme succès. | Journal d'état, identifiants d'événements et assertions idempotence. |
| P5-F05 | Résultats partiels | Simuler timeout, erreur provider, annulation demandée, perte de canal et accusé de réception perdu. | États `failed/interrupted/cancelling` adaptés ; pas de faux `succeeded` ; aucune reprise automatique non sûre. | Traces déterministes de transitions et résultat partiel conservé. |
| P5-E01 | Révision dépendance | Configurer adaptateur faux/fixture avec version attendue et version divergente. | La version attendue est tracée ; divergence/inconnue bloque le chemin REA. | Rapport de version + refus sur version mismatch. |
| P5-E02 | Contrat REA | Valider parsing avec fixtures synthétiques dérivées des schémas épinglés, erreurs et Evidence. | Contrats acceptés/refusés explicitement ; champs inconnus ou incomplets ne sont pas promus en réussite. | Fixtures, assertions de schéma, source et commit associés. |
| P5-S01 | Quarantaine import | Importer un fixture inerte, y compris nom de fichier suspect, dans l'espace de quarantaine. | Aucun lancement/processus ; aucune activation avant approbation explicite. | Audit des appels de processus et état de quarantaine. |
| P5-S02 | Sorties et secrets | Fournir canaris synthétiques marqués secrets aux erreurs et flux de logs du test harness. | Les canaris ne figurent pas dans logs, métriques, rapports ou exports non autorisés. | Recherche automatisée des canaris + rapport expurgé. |
| P5-S03 | Réseau / egress | Exécuter le harness avec réseau désactivé ou uniquement destination de test contrôlée. | Aucun transfert inattendu ; tentatives hors allowlist échouent de manière observable. | Captures de test expurgées et configuration réseau. |
| P5-D01 | Provenance / intégrité | Enregistrer fixture synthétique, transformation et rapport associé. | Empreinte, source, timestamp, version, job et lien Evidence permettent de retracer la conclusion ; altération détectée. | Manifeste + vérification d'intégrité. |
| P5-D02 | Mode sans IA | Exécuter le parcours fonctionnel sans fournisseur IA configuré. | Résultats techniques conservés ; aucun appel externe IA. | Journal d'événements et observation réseau du harness. |
| P5-D03 | Conservation / export / suppression | Avec données synthétiques, exporter puis appliquer la politique de suppression conçue. | Résultat et limites sauvegarde/audit visibles ; suppression conforme au choix accepté. | Manifeste d'export et constat de suppression/retenue. |
| P5-O01 | Accessibilité / erreurs | Parcours minimal clavier et affichage d'erreur/état sans couleur seule. | Exigences accessibles documentées satisfaites pour la portée testée. | Rapport manuel automatisable, captures anonymisées. |
| P5-O02 | Récupération | Simuler panne backend/stockage puis restaurer un jeu synthétique. | Les états incomplets sont signalés ; aucune duplication ni faux succès ; restauration vérifiée selon critères approuvés. | Journal de panne/restauration et comparaison des empreintes. |

## Règles d'acceptation et de blocage

- Un critère de sécurité critique en échec ou inconclusif bloque la recette.
- Tout test non exécuté, dépendance inconnue, faille de provenance, fuite de secret, transfert non autorisé ou succès inféré après interruption bloque la clôture.
- Les anomalies non critiques ont un ticket, propriétaire, sévérité, échéance et acceptation écrite si elles restent ouvertes.
- Une preuve doit être reproductible et référencer précisément le commit code, le SHA REA, les options, la fixture et l'environnement ; aucun résultat n'est extrapolé à un autre OS/provider.
- La revue finale compare résultats aux critères, examine les risques résiduels et consigne une décision `accepté / refusé / accepté sous réserve` par propriétaire.

## Clôture de phase 5 — checklist non cochée

- [ ] périmètre et autorisations à jour ;
- [ ] livrables réellement présents et versionnés ;
- [ ] toutes les vérifications obligatoires exécutées avec preuves ;
- [ ] aucune anomalie bloquante ou inconnue critique ;
- [ ] documentation et limitations mises à jour ;
- [ ] validation écrite du propriétaire après revue des preuves ;
- [ ] statut de roadmap modifié uniquement après ces éléments.

**Aucun test n'a été exécuté lors de la rédaction de ce protocole.**
