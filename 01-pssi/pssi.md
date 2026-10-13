# Politique de sécurité des systèmes d'information (PSSI) : Cabinet Delorme Conseil

> Document rédigé pour une entreprise fictive, dans le cadre d'un cas d'étude.
> Version 1.0, approuvée par les associés (fictif).

## 1. Objet et périmètre

Cette politique définit les règles de sécurité applicables à toutes les personnes
qui utilisent le système d'information du cabinet : associés, collaborateurs,
stagiaires, alternants et prestataires. Elle couvre les postes de travail, la messagerie,
le NAS, les applications SaaS, le portail client, le réseau et le télétravail.

## 2. Enjeux et objectifs de sécurité

Le cabinet traite des données comptables, bancaires et de paie qui sont couvertes
par le secret professionnel et le RGPD. Les objectifs sont :

- **Confidentialité** : empêcher tout accès non autorisé aux dossiers clients.
- **Intégrité** : garantir que les données comptables ne sont pas altérées.
- **Disponibilité** : rester opérationnel pendant les périodes d'échéances fiscales.
- **Conformité** : respecter le RGPD et les obligations de secret professionnel.

## 3. Rôles et responsabilités

| Rôle | Responsabilité |
|---|---|
| Associés | Approuvent la politique, allouent le budget, arbitrent les risques |
| Référent sécurité (désigné parmi les associés) | Suit l'application de la PSSI, centralise les incidents |
| Prestataire informatique | Applique les mesures techniques, rend compte au référent |
| Collaborateurs | Appliquent les règles et signalent tout incident ou comportement suspect |

## 4. Classification des informations

| Niveau | Exemples | Exigence |
|---|---|---|
| Très sensible | Paie, IBAN, numéros de sécurité sociale, relevés bancaires | Accès restreint, chiffrement, traçabilité |
| Sensible | Bilans, liasses fiscales, dossiers clients | Accès limité aux équipes concernées |
| Interne | Contrats, RH, facturation | Accès limité au personnel |

## 5. Règles de sécurité

| Réf. | Règle | Réponse à | ISO 27001:2022 |
|---|---|---|---|
| R01 | Chaque utilisateur dispose d'un compte nominatif. Les comptes partagés sont interdits. | Contrôle d'accès | 5.15 |
| R02 | L'authentification multifacteur (MFA) est obligatoire sur la messagerie, le VPN, le portail client et les applications SaaS. | MFA seulement sur la messagerie | 8.5 |
| R03 | Les mots de passe font au moins 14 caractères et sont uniques par service. Un gestionnaire de mots de passe est fourni. | Authentification | 5.17 |
| R04 | Les droits d'accès sont attribués selon le besoin d'en connaître et revus au moins une fois par an. | Droits d'accès | 5.18 |
| R05 | Les droits sont retirés le jour du départ d'un collaborateur. | Départs | 6.5 |
| R06 | Les postes sont chiffrés, à jour et protégés par un antivirus géré centralement. | Postes de travail | 8.1, 8.7 |
| R07 | Les sauvegardes du NAS suivent la règle 3-2-1 (3 copies, 2 supports, 1 hors site). Une restauration est testée au moins deux fois par an. | Sauvegardes jamais testées | 8.13 |
| R08 | Le Wi-Fi invités est isolé du réseau interne. | Wi-Fi non séparé | 8.20, 8.22 |
| R09 | Le télétravail passe par le VPN avec MFA. Les postes personnels ne doivent pas accéder aux dossiers clients. | Télétravail | 6.7 |
| R10 | Les données très sensibles ne sont jamais envoyées par e-mail en clair : on utilise le portail client ou un envoi chiffré. | Échanges de données | 5.14 |
| R11 | Le prestataire informatique signe un contrat précisant ses obligations de sécurité et de confidentialité. | Prestataires | 5.19, 5.20 |
| R12 | Tout incident ou comportement suspect (phishing, perte d'un poste, compte compromis) est signalé au référent sécurité sous 24 h. | Incidents | 5.24, 5.26 |
| R13 | Tous les collaborateurs suivent une sensibilisation à la sécurité à leur arrivée, puis une fois par an. | Pas de sensibilisation | 6.3 |
| R14 | Les données personnelles sont traitées selon le RGPD : registre des traitements, durées de conservation, information des personnes. | RGPD | 5.34 |

## 6. Application, sanctions et révision

- Cette politique s'impose à tous les utilisateurs. Un manquement peut entraîner
  des mesures disciplinaires.
- Elle est revue au moins une fois par an, ou après tout incident majeur.
- Toute dérogation doit être demandée par écrit et validée par le référent sécurité.
