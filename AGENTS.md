# Consignes de continuité du projet

Avant chaque tâche, lire `PROJECT_CONTEXT.md`, puis le document de phase active et les critères de passage de `docs/06-roadmap/roadmap.md`.

## Phase 5 — périmètre actuellement autorisé

Le propriétaire a autorisé uniquement une réalisation locale, mono-utilisateur et hors production, selon `docs/09-phase-5/implementation-authorization.md`.

Dans ce périmètre, sont autorisés :
- le code applicatif de fondations, modèles de domaine et contrats de plateforme ;
- les contrôles d'autorisation et de provenance indépendants du moteur ;
- les flux simulés avec fixtures synthétiques ;
- les tests locaux unitaires/intégration sans cible réelle, à l'aide des outils déjà disponibles.

Sont interdits jusqu'à décision et autorisation distinctes :
- installer des outils ou ajouter/télécharger des dépendances ;
- lancer ou exécuter REA ou un provider ;
- analyser une cible réelle, externe ou non explicitement autorisée ;
- exécuter des workflows dynamiques, réseau, navigateur, appareil ou modifiant une cible ;
- transférer des données vers OpenRouter, un autre fournisseur IA ou un service externe ;
- déployer en production ou exposer un service ;
- modifier le dépôt externe `morluto/rea`.

Si une tâche exige une activité interdite ci-dessus, arrêter cette activité et obtenir d'abord une décision écrite, une portée précise et la mise à jour des documents de gouvernance. L'autorisation limitée de phase 5 ne lève pas ces interdictions.

## Règles de vérité et traçabilité

- Ne pas présenter un SHA de REA comme preuve d'un audit exhaustif. Citer la révision et les sources exactes pour chaque contrat retenu ; marquer les autres éléments `inconnu`, `hypothèse` ou `non testé`.
- Séparer exigences, décisions acceptées, propositions, hypothèses et faits vérifiés.
- Ne déclarer un test exécuté ou réussi que si son exécution et son résultat sont consultables ; garder les résultats partiels et échecs distincts du succès.
- Ne pas revendiquer une phase terminée sans satisfaire ses critères et consigner la validation du propriétaire.
- Respecter les licences, la confidentialité, l'autorisation de cible et l'interdiction d'exécution automatique d'imports.

## Après chaque tâche

- Mettre à jour `PROJECT_CONTEXT.md` si état, décisions, risques ou prochaine action changent.
- Mettre à jour les documents touchés et les liens de navigation.
- Consigner les tests réellement exécutés, résultats, limites et preuves ; ne jamais inventer un résultat.
- Signaler ce qui reste ouvert et toute approbation utilisateur nécessaire.

## Porte d'extension de portée

L'intégration et l'exécution REA, les cibles réelles, les nouvelles dépendances/outils, les transferts externes et le déploiement restent bloqués jusqu'à :
1. audit documentaire détaillé des opérations REA retenues, avec source et révision ;
2. approbation spécifique du propriétaire de la cible et de l'opération lorsque pertinent ;
3. décision de sécurité/exploitation et plan de vérification compatibles ;
4. autorisation écrite actualisée dans le registre d'autorisation.
