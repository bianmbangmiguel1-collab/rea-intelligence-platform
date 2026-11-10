# Traçabilité des exigences et validation

**Statut :** cadre documentaire. Les éléments ci-dessous ne prouvent pas qu'une implémentation ou un test existe.

## Chaîne de traçabilité cible

Chaque exigence doit avoir un identifiant stable, une source, un statut, un responsable de décision, une priorité, les dépendances, un critère d'acceptation et un moyen de vérification. La chaîne attendue est :

`besoin utilisateur → exigence → conception/contrat → risque/contrôle → vérification → preuve de revue`

Une exigence dépendant de REA doit référencer le rapport et la révision audités. Tant que ceux-ci n'existent pas, elle est conditionnelle ou ouverte.

## Correspondance documentaire initiale

| Sujet | Référence | Dépendance / validation |
| --- | --- | --- |
| Parcours et exigences fonctionnelles FR-01 à FR-15 | [Spécification fonctionnelle](../01-specifications/functional-specification.md) | Priorités, rôles et pilote à confirmer |
| Composants et attribution des jobs | [Architecture détaillée](../02-architecture/detailed-architecture.md) | Transport agent et adaptateur REA non confirmés |
| Menaces et contrôles | [Conception sécurité](../02-architecture/security-design.md), [registre des risques](risk-register.md) | Contrôles d'exploitation à compléter en phase 3 |
| Concepts métier | [Modèle de données](../04-data-model/data-model.md) | Politique de rétention et schéma physique non décidés |
| API plateforme | [Contrats API proposés](../05-api-contracts/api-contracts.md) | Auth, erreurs, pagination et versionnage à valider |
| Données et appels IA | [Gouvernance données/IA](data-ai-governance.md) | Fournisseur, consentement et rétention ouverts |
| Capacités et interfaces du moteur | [Plan d'audit REA](rea-audit-plan.md) | Aucun fait REA vérifié enregistré |

## Statut de vérification

Employer une formulation non ambiguë :

- **À concevoir** : proposition non validée.
- **À auditer** : dépendance externe ou fait technique non vérifié.
- **À valider** : décision ou revue attendue du propriétaire.
- **Planifié** : vérification décrite, mais non exécutée.
- **Vérifié** : preuve consultable, datée et associée à une version précise.
- **Bloqué** : prérequis manquant ; indiquer lequel.

Ne pas utiliser « réussi », « compatible », « sécurisé » ou « prêt » sans préciser la portée, la version, les critères et les preuves.

## Vérification ultérieure

Après autorisation d'entrer en réalisation, les contrôles devront couvrir les critères fonctionnels et sécurité, les droits inter-projets, les autorisations et échéances, révocation, intégrité/provenance, données IA, reprise/annulation, accessibilité et sauvegarde/restauration. Les environnements, jeux de données, cibles et limites devront être explicitement autorisés et non réels par défaut. Aucun test de cette nature n'est effectué par le présent livrable documentaire.

## Revue de phase

Une revue de phase consigne : versions des documents examinés, décisions acceptées/rejetées, points ouverts et propriétaires, risques résiduels, dérogations, validation utilisateur et décision de passage. La roadmap demeure l'autorité sur les portes ; un document rédigé ne signifie pas que sa porte est franchie.
