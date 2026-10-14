# Analyse de risques EBIOS RM : Atelier 5, traitement du risque

> Cas d'étude fictif : Cabinet Delorme Conseil. Fait suite aux ateliers 1 à 4.
> Niveau de risque = gravité × vraisemblance : 12 ou plus = critique, 8 à 11 = élevé, 4 à 7 = moyen, moins de 4 = faible.

## 1. Synthèse des risques avant traitement

| Scénario | Description | Gravité | Vraisemblance | Niveau |
|---|---|---|---|---|
| SS1 / SO1 | Ransomware via le prestataire informatique | G4 | 3 | Critique (12) |
| SS2 / SO2 | Ransomware via hameçonnage | G4 | 3 | Critique (12) |
| SS3 | Fraude au virement via un client compromis | G3 | 3 | Élevé (9) |
| SS4 | Fuite de données par un salarié malveillant | G4 | 2 | Élevé (8) |

## 2. Plan de traitement

Les mesures des ateliers 3 et 4 sont regroupées en actions.

| Réf. | Action | Mesures regroupées | Scénarios | PSSI | Priorité | Échéance | Coût | Responsable |
|---|---|---|---|---|---|---|---|---|
| T1 | Sécuriser l'accès du prestataire : MFA, compte nominatif limité dans le temps, clauses de sécurité au contrat, journalisation de ses accès | M1, M2, M7 | SS1 | R01, R02, R04, R11 | 1 | 1 mois | Faible | Référent sécurité |
| T2 | Mettre en place une sauvegarde hors ligne et tester la restauration deux fois par an | M6, M12 | SS1, SS2 | R07 | 1 | 1 mois | Moyen | Prestataire informatique |
| T3 | Généraliser la MFA à la messagerie, au VPN, au portail client et aux applications SaaS | (socle) | SS1, SS2, SS3 | R02 | 1 | 1 mois | Faible | Prestataire informatique |
| T4 | Imposer une vérification par téléphone avant toute modification d'IBAN ou paiement inhabituel | M4 | SS3 | R10, R12 | 1 | 2 semaines | Nul | Associés |
| T5 | Sensibiliser les collaborateurs et organiser des simulations de hameçonnage | M3, M10 | SS2, SS3 | R13 | 2 | 3 mois | Faible | Référent sécurité |
| T6 | Déployer un antivirus géré centralement sur tous les postes | M11 | SS2 | R06 | 2 | 3 mois | Moyen | Prestataire informatique |
| T7 | Cloisonner le NAS par équipe et isoler le Wi-Fi invités | M8 | SS1, SS2, SS4 | R04, R08 | 2 | 3 mois | Moyen | Prestataire informatique |
| T8 | Journaliser les accès au NAS et alerter sur les copies massives de fichiers | M5, M9 | SS1, SS4 | R12 | 3 | 6 mois | Moyen | Prestataire informatique |

Les actions de priorité 1 sont peu coûteuses et réduisent le plus les risques critiques : elles se font en premier.

## 3. Risques résiduels

| Scénario | Niveau initial | Actions appliquées | Vraisemblance après | Niveau résiduel | Décision |
|---|---|---|---|---|---|
| SS1 / SO1 | Critique (12) | T1, T2, T3, T7, T8 | 2 | Élevé (G4 × 2 = 8) | Accepté temporairement, revue à 6 mois |
| SS2 / SO2 | Critique (12) | T2, T3, T5, T6, T7 | 2 | Élevé (G4 × 2 = 8) | Accepté temporairement, revue à 6 mois |
| SS3 | Élevé (9) | T3, T4, T5 | 2 | Moyen (G3 × 2 = 6) | Accepté |
| SS4 | Élevé (8) | T7, T8 | 1 | Moyen (G4 × 1 = 4) | Accepté |

La gravité des scénarios de ransomware reste à G4 : une fuite de données reste grave même
si la sauvegarde limite l'indisponibilité. Seule la vraisemblance baisse.

## 4. Décision d'acceptation

Les risques résiduels élevés (SS1 et SS2) sont acceptés par les associés (fictif) à condition que
les actions de priorité 1 soient terminées sous un mois et que le plan soit revu dans six mois.
Le risque est réévalué après tout incident majeur ou changement important du système d'information.

## 5. Suivi

| Indicateur | Cible | Fréquence |
|---|---|---|
| Part des accès avec MFA | 100 % | Mensuelle |
| Date du dernier test de restauration | Moins de 6 mois | Semestrielle |
| Part des collaborateurs formés | 100 % | Annuelle |
| Taux de clics lors des simulations de hameçonnage | Moins de 10 % | Par campagne |
| Nombre d'incidents signalés et traités | Suivi, aucun en retard | Mensuelle |
