# Audit ISO 27001 : plan d'action

> Cas d'étude fictif : Cabinet Delorme Conseil. Fait suite aux constats (`02-constats.md`).
> Les actions reprennent celles du plan de traitement EBIOS RM (`T1` à `T8`) quand elles existent déjà.
> Priorité 1 = à traiter en premier (non-conformités majeures), 3 = à planifier.

## 1. Non-conformités majeures

| Réf. | Écart | Action corrective | Lien EBIOS RM | Priorité | Échéance | Responsable | Preuve de clôture |
|---|---|---|---|---|---|---|---|
| A1 | 8.5 : MFA incomplète | Activer la MFA sur le VPN, le portail client et les applications SaaS | T3 | 1 | 1 mois | Prestataire informatique | Capture de la configuration, test de connexion |
| A2 | 5.19, 5.20 : contrat prestataire sans exigences de sécurité | Avenant au contrat : MFA, compte nominatif, journalisation, notification d'incident sous 24 h | T1 | 1 | 1 mois | Associés, référent sécurité | Avenant signé |
| A3 | 8.13 : sauvegardes non testées, pas de copie hors ligne | Ajouter une sauvegarde hors ligne, tester la restauration | T2 | 1 | 1 mois | Prestataire informatique | Compte rendu d'un test de restauration réussi |
| A4 | 6.3 : pas de sensibilisation | Première session de sensibilisation, puis simulation de hameçonnage | T5 | 1 | 3 mois | Référent sécurité | Liste d'émargement, résultats de la simulation |

## 2. Non-conformités mineures

| Réf. | Écart | Action corrective | Lien EBIOS RM | Priorité | Échéance | Responsable | Preuve de clôture |
|---|---|---|---|---|---|---|---|
| A5 | 5.24 : pas de gestion des incidents | Rédiger une procédure de signalement et un registre des incidents | PSSI R12 | 2 | 2 mois | Référent sécurité | Procédure diffusée au personnel |
| A6 | 5.15 : compte partagé sur le logiciel de paie | Créer des comptes nominatifs, supprimer le compte partagé | PSSI R01 | 2 | 1 mois | Prestataire informatique | Liste des comptes avant et après |
| A7 | 5.17 : mots de passe faibles | Imposer 14 caractères minimum et fournir un gestionnaire de mots de passe | PSSI R03 | 2 | 2 mois | Prestataire informatique | Politique appliquée, outil déployé |
| A8 | 8.22 : Wi-Fi invités non cloisonné | Isoler le Wi-Fi invités du réseau interne | T7 | 2 | 3 mois | Prestataire informatique | Test d'isolation |
| A9 | 8.7 : antivirus non centralisé | Déployer un antivirus géré centralement | T6 | 2 | 3 mois | Prestataire informatique | Console de gestion avec tous les postes |
| A10 | 6.1.3 : pas de déclaration d'applicabilité | Rédiger la déclaration d'applicabilité à partir de l'analyse de risques | EBIOS RM | 2 | 2 mois | Référent sécurité | Document approuvé |
| A11 | 8.15 : pas de journalisation | Journaliser les accès au NAS, avec alerte sur les copies massives | T8 | 3 | 6 mois | Prestataire informatique | Extrait de journal, test d'alerte |
| A12 | 5.18 : droits jamais revus | Instaurer une revue annuelle des droits d'accès | PSSI R04 | 3 | 6 mois | Référent sécurité | Compte rendu de revue |
| A13 | 9.3 : pas de revue de direction | Planifier une revue annuelle par les associés | ISO 27001 art. 9.3 | 3 | 6 mois | Associés | Compte rendu signé |

## 3. Observations à traiter

| Réf. | Observation | Action | Échéance |
|---|---|---|---|
| O1 | 6.5 : départs sans procédure écrite | Rédiger une procédure de départ (retrait des accès le jour même) | 6 mois |
| O2 | 9.2 : pas de programme d'audit | Établir un programme d'audit interne annuel | 6 mois |
| O3 | 5.34 : registre RGPD incomplet | Compléter le registre des traitements | 6 mois |

## 4. Suivi

- **À un mois** : contrôle de A1, A2, A3 et A6.
- **À trois mois** : contrôle de A4, A8 et A9.
- **À six mois** : audit de suivi complet, vérification de la clôture de toutes les actions, mise à jour de l'analyse de risques et revue de direction.

## 5. Conclusion

Le cabinet dispose d'une politique de sécurité et d'une analyse de risques solides, mais l'application sur le terrain est en retard : quatre non-conformités majeures, toutes liées aux risques les plus élevés de l'analyse, sont à traiter en priorité. La plupart des actions sont peu coûteuses et réalisables en moins de trois mois. Le dispositif devra ensuite être revu chaque année pour rester efficace.
