# Analyse de risques EBIOS RM : Atelier 4, scénarios opérationnels

> Cas d'étude fictif : Cabinet Delorme Conseil. Fait suite à l'atelier 3.
> Les identifiants de techniques (Txxxx) viennent du référentiel MITRE ATT&CK.
> Les descriptions restent volontairement de haut niveau : l'objectif est de défendre, pas d'attaquer.

## 1. Échelle de probabilité de succès d'une étape

| Niveau | Signification |
|---|---|
| 1 | Très improbable : l'attaquant échoue presque toujours |
| 2 | Peu probable : des mesures sérieuses existent |
| 3 | Probable : les mesures sont partielles |
| 4 | Quasi certain : aucune mesure efficace |

## 2. Scénario SO1 : ransomware via le prestataire informatique (issu de SS1)

| Phase | Action de l'attaquant | Technique ATT&CK | Succès | Mesure existante ou manquante |
|---|---|---|---|---|
| Connaître | Repérer le prestataire et ses outils d'accès à distance | T1589 (collecte d'informations sur la victime) | 4 | Impossible à empêcher : informations publiques |
| Rentrer | Compromettre le prestataire puis utiliser son accès légitime au cabinet | T1199 (relation de confiance), T1078 (comptes valides) | 3 | MFA absente sur les accès du prestataire, contrat sans obligations de sécurité |
| Trouver | Parcourir le réseau, repérer le NAS et les partages | T1135 (découverte des partages réseau), T1087 (découverte de comptes) | 3 | Pas de segmentation interne ni de journalisation des accès |
| Exploiter | Copier les données pour la double extorsion, puis chiffrer le NAS | T1567 (exfiltration via un service web), T1486 (chiffrement à des fins d'impact) | 3 | Sauvegardes jamais testées, pas de sauvegarde hors ligne |

**Vraisemblance du scénario : 3 (probable).**
Points de détection possibles : connexion du prestataire hors des horaires habituels, volume de fichiers copiés inhabituel, apparition de fichiers chiffrés.

## 3. Scénario SO2 : ransomware via hameçonnage (issu de SS2)

| Phase | Action de l'attaquant | Technique ATT&CK | Succès | Mesure existante ou manquante |
|---|---|---|---|---|
| Connaître | Identifier les collaborateurs et leurs adresses e-mail | T1589 (collecte d'informations sur la victime) | 4 | Informations publiques (site, réseaux sociaux) |
| Rentrer | Envoyer un e-mail piégé, obtenir l'ouverture d'une pièce jointe ou d'un lien | T1566 (hameçonnage), T1204 (exécution par l'utilisateur) | 3 | Aucune sensibilisation du personnel |
| Trouver | Voler des identifiants et se déplacer vers le NAS | T1003 (récupération d'identifiants), T1021 (services distants) | 2 | Antivirus présent mais non géré centralement |
| Exploiter | Désactiver les restaurations possibles puis chiffrer les données | T1490 (suppression des moyens de récupération), T1486 (chiffrement) | 3 | Sauvegardes jamais testées |

**Vraisemblance du scénario : 3 (probable).**
Points de détection possibles : e-mail suspect signalé par un collaborateur, alerte antivirus, arrêt brutal des sauvegardes.

## 4. Mesures complémentaires proposées

| Réf. | Mesure | Maillon visé | Scénarios | Règle de la PSSI |
|---|---|---|---|---|
| M7 | Exiger la MFA et un compte nominatif pour tout accès du prestataire | Rentrer | SO1 | R01, R02, R11 |
| M8 | Cloisonner le NAS : accès limité par équipe et segmentation du réseau | Trouver | SO1, SO2 | R04, R08 |
| M9 | Journaliser les accès et les copies de fichiers, avec alerte en cas de volume anormal | Trouver, Exploiter | SO1 | R12 |
| M10 | Campagnes de sensibilisation et de simulation de hameçonnage | Rentrer | SO2 | R13 |
| M11 | Antivirus avec gestion centralisée sur tous les postes | Rentrer, Trouver | SO2 | R06 |
| M12 | Sauvegarde hors ligne et test de restauration deux fois par an | Exploiter | SO1, SO2 | R07 |

## 5. Synthèse

Dans les deux scénarios, la phase finale (chiffrement) est difficile à arrêter une fois atteinte.
Les mesures sont donc concentrées sur les phases **Rentrer** et **Trouver**, ainsi que sur la capacité
de restauration, qui limite l'impact si l'attaque réussit. Ces mesures alimentent l'atelier 5.
