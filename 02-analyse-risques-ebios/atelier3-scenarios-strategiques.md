# Analyse de risques EBIOS RM : Atelier 3, scénarios stratégiques

> Cas d'étude fictif : Cabinet Delorme Conseil. Fait suite aux ateliers 1 et 2.

## 1. Cartographie de l'écosystème

Chaque critère est noté de 1 (faible) à 4 (très fort).
Dangerosité = (dépendance × pénétration) / (maturité cyber × confiance).
Seuils simplifiés choisis pour cette étude : 2 ou plus = zone de danger, de 1 à moins de 2 = zone de contrôle, moins de 1 = zone de veille.

| Réf. | Partie prenante | Dépendance | Pénétration | Maturité | Confiance | Dangerosité | Zone |
|---|---|---|---|---|---|---|---|
| PP1 | Prestataire informatique (infogérance, accès administrateur) | 3 | 4 | 2 | 3 | 2,0 | Danger |
| PP2 | Éditeur du logiciel de comptabilité et de paie (SaaS) | 4 | 3 | 3 | 3 | 1,3 | Contrôle |
| PP3 | Fournisseur de messagerie cloud (Microsoft 365) | 4 | 3 | 4 | 3 | 1,0 | Contrôle |
| PP4 | Prestataire du portail client | 2 | 3 | 2 | 2 | 1,5 | Contrôle |
| PP5 | Clients (envoi de pièces et d'e-mails) | 2 | 2 | 1 | 2 | 2,0 | Danger |

Les parties prenantes en zone de danger (PP1 et PP5) sont les premières à traiter.

## 2. Scénarios stratégiques

Échelle de vraisemblance : 1 (très peu probable) à 4 (très probable).
Niveau de risque = gravité × vraisemblance : 12 ou plus = critique, 8 à 11 = élevé, 4 à 7 = moyen, moins de 4 = faible.

| Réf. | Couple | Chemin d'attaque | Événements redoutés | Gravité | Vraisemblance | Niveau |
|---|---|---|---|---|---|---|
| SS1 | SR1 / OV1 | Le groupe de ransomware compromet le prestataire informatique (PP1), utilise son accès à distance pour entrer dans le SI du cabinet, exfiltre puis chiffre les données du NAS | ER1, ER2, ER3 | G4 | 3 | Critique (12) |
| SS2 | SR1 / OV1 | Un e-mail de hameçonnage piège un collaborateur, l'attaquant prend le contrôle du poste, atteint le NAS et déclenche le chiffrement | ER1, ER2, ER3 | G4 | 3 | Critique (12) |
| SS3 | SR2 / OV2 | L'attaquant compromet la messagerie d'un client (PP5), envoie au cabinet de fausses demandes de paiement ou de faux IBAN | ER5 | G3 | 3 | Élevé (9) |
| SS4 | SR4 / OV4 | Un salarié malveillant utilise ses accès légitimes pour copier des dossiers clients depuis le NAS, sans que personne ne le détecte | ER1, ER2 | G4 | 2 | Élevé (8) |

## 3. Mesures de sécurité sur l'écosystème

| Réf. | Mesure | Parties prenantes et scénarios visés | Règle de la PSSI |
|---|---|---|---|
| M1 | Ajouter au contrat du prestataire des obligations de sécurité (MFA obligatoire, journalisation de ses accès, notification d'incident sous 24 h) | PP1, SS1 | R11, R02 |
| M2 | Exiger un accès du prestataire par compte nominatif et limité dans le temps | PP1, SS1 | R01, R04 |
| M3 | Former les collaborateurs au hameçonnage, avec des campagnes de test | SS2, SS3 | R13 |
| M4 | Imposer une vérification par téléphone avant toute modification d'IBAN ou tout paiement inhabituel | PP5, SS3 | R10, R12 |
| M5 | Journaliser les accès au NAS et alerter sur les copies massives de fichiers | SS4 | R04, R12 |
| M6 | Mettre en place des sauvegardes hors ligne et tester leur restauration | SS1, SS2 | R07 |

## 4. Scénarios retenus pour l'atelier 4

Les scénarios SS1 et SS2 (niveau critique) sont retenus pour être détaillés techniquement dans l'atelier 4.
SS3 et SS4 sont traités par les mesures ci-dessus et suivis.
