# Analyse de risques EBIOS RM : Atelier 2, sources de risques

> Cas d'étude fictif : Cabinet Delorme Conseil. Fait suite à l'atelier 1 (`atelier1-cadrage.md`).

## 1. Sources de risques et objectifs visés

| Réf. | Source de risque | Objectif visé | Événements redoutés concernés |
|---|---|---|---|
| SR1 | Cybercriminel organisé (groupe de ransomware) | OV1 : extorquer de l'argent en chiffrant les systèmes et en menaçant de publier les données | ER1, ER2, ER3 |
| SR2 | Cybercriminel spécialisé dans la fraude (usurpation d'identité, fraude au virement) | OV2 : détourner des fonds en se faisant passer pour le cabinet ou l'un de ses clients | ER5 |
| SR3 | Cabinet concurrent | OV3 : récupérer le portefeuille de clients et les informations commerciales | ER2 |
| SR4 | Salarié ou ex-salarié malveillant | OV4 : voler ou divulguer des dossiers clients par vengeance ou pour les revendre | ER1, ER2 |
| SR5 | Attaquant opportuniste (scans automatisés) | OV5 : prendre le contrôle d'un système exposé (portail, VPN) pour le revendre ou s'en servir | ER3 |

## 2. Évaluation de la pertinence

Grille simplifiée, inspirée de la méthode : chaque critère est noté de 1 (faible) à 4 (très fort).
La pertinence est une appréciation d'ensemble de la motivation, des ressources et de l'activité de la source.

| Couple | Motivation | Ressources | Activité | Pertinence | Retenu |
|---|---|---|---|---|---|
| SR1 / OV1 | 4 | 3 | 4 | Très forte | Oui |
| SR2 / OV2 | 4 | 3 | 3 | Forte | Oui |
| SR3 / OV3 | 2 | 2 | 1 | Faible | Non |
| SR4 / OV4 | 2 | 3 | 2 | Moyenne | Oui |
| SR5 / OV5 | 2 | 2 | 4 | Moyenne | Non (traité par les mesures de base) |

## 3. Justification des choix

- **SR1 / OV1 retenu** : les cabinets comptables manipulent des données très sensibles et subissent des échéances fixes, ce qui en fait des cibles rentables pour l'extorsion.
- **SR2 / OV2 retenu** : le cabinet gère des relevés bancaires et des demandes de paiement, ce qui expose à la fraude au virement.
- **SR4 / OV4 retenu** : un salarié a naturellement accès aux dossiers sans avoir besoin de s'introduire dans le système. Le niveau reste moyen, mais il est cohérent avec le secret professionnel en jeu.
- **SR3 / OV3 écarté** : l'espionnage entre cabinets est peu probable et peu documenté. Il est suivi mais ne donne pas lieu à un scénario détaillé.
- **SR5 / OV5 écarté** : le risque est réel mais déjà couvert par les mesures de base de la PSSI (R02 pour la MFA, R06 pour les mises à jour des postes).

## 4. Couples retenus pour l'atelier 3

1. SR1 / OV1 : extorsion par ransomware
2. SR2 / OV2 : fraude au virement
3. SR4 / OV4 : fuite de données par un salarié malveillant
