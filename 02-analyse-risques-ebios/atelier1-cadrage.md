# Analyse de risques EBIOS RM : Atelier 1, cadrage et socle de sécurité

> Cas d'étude fictif : Cabinet Delorme Conseil (voir `00-presentation-pme`).

## 1. Cadre de l'étude

- **Objectif** : identifier et traiter les risques pesant sur les missions du cabinet.
- **Périmètre** : l'ensemble du système d'information du cabinet (postes, messagerie, NAS, applications SaaS, portail client, VPN, réseau) et le personnel qui l'utilise.
- **Méthode** : EBIOS Risk Manager (ANSSI).
- **Participants (fictifs)** : un associé, le prestataire informatique, un responsable de dossiers comptables.

## 2. Échelle de gravité

| Niveau | Gravité | Conséquences pour le cabinet |
|---|---|---|
| G1 | Mineure | Gêne ponctuelle, sans impact sur les clients |
| G2 | Significative | Retard de traitement, quelques clients mécontents |
| G3 | Grave | Violation de données ou manquement aux échéances fiscales, risque de sanction et de perte de clients |
| G4 | Critique | Atteinte au secret professionnel à grande échelle, mise en cause de l'existence du cabinet |

## 3. Valeurs métier et biens supports

| Valeur métier | Description | Biens supports |
|---|---|---|
| VM1 : Tenue comptable et fiscale | Production des comptes, bilans et déclarations des clients | Logiciel de comptabilité SaaS, NAS, postes de travail, messagerie |
| VM2 : Gestion de la paie | Production des bulletins et déclarations sociales | Logiciel de paie SaaS, postes des gestionnaires, NAS |
| VM3 : Échanges avec les clients | Dépôt des pièces et communication sécurisée | Portail client, messagerie, VPN |

Biens supports communs : réseau et Wi-Fi, prestataire informatique, personnel du cabinet.

## 4. Événements redoutés

| Réf. | Événement redouté | Valeur métier | Critère | Gravité | Justification |
|---|---|---|---|---|---|
| ER1 | Fuite des données de paie (IBAN, numéros de sécurité sociale) | VM2 | Confidentialité | G4 | Données personnelles très sensibles, sanctions RGPD, perte de confiance |
| ER2 | Fuite de dossiers comptables et fiscaux de clients | VM1 | Confidentialité | G4 | Atteinte au secret professionnel |
| ER3 | Indisponibilité du système d'information en période d'échéances fiscales | VM1, VM2 | Disponibilité | G3 | Retards de déclarations, pénalités pour les clients |
| ER4 | Altération de données comptables ou de paie | VM1, VM2 | Intégrité | G3 | Déclarations erronées, responsabilité du cabinet engagée |
| ER5 | Usurpation d'un compte ou détournement d'une demande de paiement | VM3 | Intégrité | G3 | Fraude possible chez les clients |

## 5. Socle de sécurité

| Domaine | Mesure attendue | État | Écart |
|---|---|---|---|
| Authentification | MFA sur tous les accès sensibles | Partiel | MFA uniquement sur la messagerie |
| Sauvegardes | Règle 3-2-1 et restaurations testées | Partiel | Sauvegardes jamais testées en restauration |
| Réseau | Segmentation du Wi-Fi invités | Non appliqué | Wi-Fi invités non séparé |
| Sensibilisation | Formation annuelle du personnel | Non appliqué | Aucune sensibilisation |
| Gouvernance | Politique de sécurité formalisée | Appliqué | PSSI rédigée (voir `01-pssi`) |
| Prestataire | Obligations de sécurité dans le contrat | Partiel | Contrat à compléter |

## 6. Synthèse

Les événements ER1 et ER2 (fuites de données) sont les plus graves. Le socle de
sécurité présente des écarts importants (MFA, sauvegardes, réseau, sensibilisation)
qui alimenteront les scénarios des ateliers suivants.
