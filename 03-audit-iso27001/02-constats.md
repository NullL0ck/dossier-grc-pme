# Audit ISO 27001 : constats

> Cas d'étude fictif : Cabinet Delorme Conseil. Audit interne à blanc, sans valeur de certification.
> État constaté avant la mise en œuvre du plan de traitement (`02-analyse-risques-ebios`).
> Les preuves sont fictives. Les contrôles de sécurité physique (thème 7 de l'annexe A) ne sont pas audités dans cette version.

## 1. Constats sur les exigences de la norme (articles 4 à 10)

| Réf. | Exigence | Preuves | Résultat | Type d'écart |
|---|---|---|---|---|
| 5.2 | Politique de sécurité de l'information | PSSI v1.0 approuvée par les associés | Conforme | Aucun |
| 6.1.2 | Appréciation des risques de sécurité | Analyse EBIOS RM complète (ateliers 1 à 5) | Conforme | Aucun |
| 6.1.3 | Traitement des risques et déclaration d'applicabilité | Plan de traitement présent, déclaration d'applicabilité absente | Partiellement conforme | Non-conformité mineure |
| 9.2 | Audit interne | Premier audit, réalisé à blanc, sans programme d'audit établi | Partiellement conforme | Observation |
| 9.3 | Revue de direction | Aucune revue formelle du dispositif par les associés | Non conforme | Non-conformité mineure |

## 2. Constats sur les mesures de l'annexe A

| Réf. | Mesure | Règle PSSI | Preuves | Résultat | Type d'écart |
|---|---|---|---|---|---|
| 5.15 | Contrôle d'accès | R01 | Comptes nominatifs sur la messagerie, mais un compte partagé sur le logiciel de paie | Partiellement conforme | Non-conformité mineure |
| 5.17 | Informations d'authentification | R03 | Mots de passe de 8 caractères minimum, pas de gestionnaire de mots de passe | Partiellement conforme | Non-conformité mineure |
| 8.5 | Authentification sécurisée | R02 | MFA activée uniquement sur la messagerie, ni sur le VPN, ni sur le portail client, ni sur les applications SaaS | Partiellement conforme | **Non-conformité majeure** |
| 5.18 | Droits d'accès | R04 | Droits attribués à l'arrivée, jamais revus depuis | Partiellement conforme | Non-conformité mineure |
| 6.5 | Fin ou changement d'emploi | R05 | Retrait des accès fait au cas par cas, sans procédure écrite | Partiellement conforme | Observation |
| 8.13 | Sauvegarde des informations | R07 | Sauvegarde nocturne du NAS sur disque externe, jamais testée en restauration, pas de copie hors ligne | Partiellement conforme | **Non-conformité majeure** |
| 8.22 | Cloisonnement des réseaux | R08 | Wi-Fi invités et réseau interne sur le même réseau | Non conforme | Non-conformité mineure |
| 6.3 | Sensibilisation et formation | R13 | Aucune sensibilisation du personnel depuis la création du cabinet | Non conforme | **Non-conformité majeure** |
| 5.19, 5.20 | Fournisseurs et accords avec les fournisseurs | R11 | Contrat d'infogérance sans clause de sécurité ni de notification d'incident | Non conforme | **Non-conformité majeure** |
| 8.7 | Protection contre les programmes malveillants | R06 | Antivirus présent sur les postes, mais non géré de façon centralisée | Partiellement conforme | Non-conformité mineure |
| 5.24 | Gestion des incidents | R12 | Aucune procédure de signalement ni de réponse aux incidents | Non conforme | Non-conformité mineure |
| 8.15 | Journalisation | (plan T8) | Aucune journalisation des accès au NAS | Non conforme | Non-conformité mineure |
| 5.34 | Protection de la vie privée et des données personnelles | R14 | Registre des traitements RGPD incomplet | Partiellement conforme | Observation |

## 3. Synthèse

| Résultat | Nombre |
|---|---|
| Conforme | 2 |
| Partiellement conforme | 10 |
| Non conforme | 6 |
| **Total** | **18** |

| Type d'écart | Nombre |
|---|---|
| Non-conformité majeure | 4 |
| Non-conformité mineure | 9 |
| Observation | 3 |
| Aucun écart | 2 |

## 4. Lien avec l'analyse de risques

Les quatre non-conformités majeures correspondent aux faiblesses exploitées dans les scénarios critiques d'EBIOS RM :

| Non-conformité majeure | Scénarios concernés | Action du plan de traitement |
|---|---|---|
| 8.5 : MFA incomplète | SS1, SS2, SS3 | T3 |
| 8.13 : sauvegardes non testées | SS1, SS2 | T2 |
| 6.3 : pas de sensibilisation | SS2, SS3 | T5 |
| 5.19, 5.20 : contrat prestataire sans exigences de sécurité | SS1 | T1 |

Les écarts les plus graves de l'audit recoupent donc les risques les plus élevés de l'analyse, ce qui confirme la cohérence du dossier.
