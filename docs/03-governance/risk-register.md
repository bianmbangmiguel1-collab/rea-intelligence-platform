# Registre initial des risques

**Statut :** registre de conception préliminaire. Probabilité, impact, propriétaire et acceptation des risques restent à évaluer avec le propriétaire du projet ; aucune mesure n'a été testée.

| ID | Risque | Conséquence | Réponse de conception proposée | État / décision requise |
| --- | --- | --- | --- | --- |
| R-01 | Périmètre ou autorisation absent, expiré ou ambigu | Analyse non autorisée ou hors cible | Blocage par défaut ; lier autorisation, cible, action, durée et exclusions ; revalider avant exécution | Politique du pilote à valider |
| R-02 | Capacités REA présumées sans preuve de version | Mauvaise attribution, échec ou exposition inattendue | Audit d'une révision précise ; adaptateur versionné ; inconnues visibles | Audit phase 1 ouvert |
| R-03 | Ressource importée malveillante | Compromission de l'environnement ou des données | Quarantaine, inspection, approbation et isolation à concevoir | Architecture phase 3 à détailler |
| R-04 | Accès réseau hors périmètre depuis un agent | Atteinte d'une destination non autorisée | Politique de destination au point d'exécution ; limites et approbations à définir | Modèle d'exécution ouvert |
| R-05 | Vol ou compromission d'agent | Exécution ou accès non autorisé | Identité par agent, moindre privilège, révocation, mises à jour et journalisation à concevoir | Enrôlement/révocation ouverts |
| R-06 | Fuite de données vers un fournisseur IA | Divulgation de données confidentielles ou personnelles | Pas de transfert implicite ; minimisation, consentement, filtrage, budget et mode sans IA | Fournisseur et politique non choisis |
| R-07 | Prompt injection via contenu analysé | Instructions non fiables influencent une action | Traiter les résultats comme données ; aucune autorité d'exécution ou d'approbation à l'IA | Exigence à conserver et tester ultérieurement |
| R-08 | Perte ou altération de preuves | Conclusions invérifiables ou rapports trompeurs | Provenance, empreintes, versionnement, sauvegardes et accès contrôlé à concevoir | Rétention/restauration ouvertes |
| R-09 | Dépendances, licences ou changements upstream | Blocage juridique, incompatibilité ou risque supply chain | Épingler les versions ; revue des licences et provenance ; plan de mise à jour | Dépend de l'audit et du modèle d'exploitation |
| R-10 | Reprise incorrecte après interruption | Succès déclaré sans preuve ou opérations dupliquées | États explicites, idempotence, résultats partiels et reprise contrôlée | Contrats à préciser |
| R-11 | Secrets présents dans logs, rapports ou prompts | Compromission durable d'accès | Minimisation, masquage, contrôle des journaux et rotation à concevoir | Vérification à planifier en phase 3 |
| R-12 | Portée du pilote ou coûts non bornés | Dépenses, délai ou maintenance imprévus | Définir scénarios, limites de budget et conditions de sortie avant réalisation | Décision utilisateur requise |

## Suivi et règle de traitement

Ajouter pour chaque risque : propriétaire, vraisemblance, impact, niveau, traitement (réduire/éviter/transférer/accepter), échéance et preuve de fermeture. Ne jamais fermer un risque sur la seule base d'une intention documentaire. Toute acceptation doit être explicite et datée. Les risques de sécurité critiques non traités bloquent la porte de réalisation.
