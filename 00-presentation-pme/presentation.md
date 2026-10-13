# Présentation de la PME : Cabinet Delorme Conseil (entreprise fictive)


> Cas d'étude fictif réalisé dans le cadre de ma formation en cybersécurité.
> Toute ressemblance avec une entreprise réelle serait fortuite.

## 1. Identité

| Élément | Détail |
|---|---|
| Activité | Expertise comptable : tenue comptable, paie, bilans, conseil fiscal |
| Effectif | 30 salariés (2 associés, 18 collaborateurs comptables, 4 gestionnaires de paie, 3 administratifs, 3 stagiaires et alternants) |
| Clients | Environ 400 TPE/PME et artisans |
| Implantation | 1 site unique, locaux loués |
| Télétravail | 2 jours par semaine pour les collaborateurs |

## 2. Système d'information

| Composant | Description |
|---|---|
| Postes de travail | 30 PC portables Windows 11 |
| Messagerie | Microsoft 365 (messagerie, agenda, Teams) |
| Stockage | 1 NAS sur site pour les dossiers clients, sauvegarde nocturne sur disque externe |
| Logiciels métier | Logiciel de comptabilité et de paie en mode SaaS |
| Portail client | Site web permettant aux clients de déposer leurs pièces comptables |
| Accès à distance | VPN pour accéder au NAS en télétravail |
| Réseau | 1 box professionnelle, Wi-Fi interne et Wi-Fi invités non séparés |
| Informatique | Infogérance externe, intervention 1 jour par semaine |

## 3. Données à protéger

| Type de données | Exemples | Sensibilité |
|---|---|---|
| Données comptables et fiscales | Bilans, liasses, déclarations | Élevée (secret professionnel) |
| Données de paie | Bulletins, IBAN, numéros de sécurité sociale | Très élevée (données personnelles) |
| Données bancaires clients | Relevés, accès aux comptes | Très élevée |
| Données internes | Contrats, RH, facturation | Moyenne |

## 4. Contexte réglementaire

- **RGPD** : le cabinet traite des données personnelles (clients et salariés de ses clients).
- **Secret professionnel** de l'expert-comptable.
- **NIS2** : applicabilité à étudier (le cabinet est probablement hors périmètre direct, à justifier dans l'analyse).

## 5. Niveau de maturité actuel en sécurité

- Pas de RSSI, pas de politique de sécurité formalisée.
- MFA activée uniquement sur la messagerie.
- Sauvegardes présentes mais jamais testées en restauration.
- Pas de sensibilisation du personnel à la sécurité.
- Budget sécurité limité, décisions prises par les associés.

## 6. Hypothèses et limites

Ce dossier est un cas d'étude : les données ci-dessus sont inventées et simplifiées.
