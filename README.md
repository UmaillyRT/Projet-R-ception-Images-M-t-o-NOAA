# 📡 Projet : Réception d'Images Météo NOAA (SDR)

**Contexte :** SAE3.ROM.04 - IUT La Réunion  
**Équipe :** Harry ARAUX, Brice BERNARDIN, Ulrick MAILLY  
**Technologie :** Radio Logicielle (SDR)

---

## 🎯 Objectif du Projet

L'objectif principal de ce TP était de mettre en œuvre une **chaîne complète de réception satellite au sol**. Il s'agissait d'intercepter les signaux radio (APT - *Automatic Picture Transmission*) émis par les satellites défilants **NOAA** (15, 18 et 19) pour les décoder et reconstituer des cartes météorologiques en temps réel.

---

## 🛠️ Matériel et Outils Déployés

Pour réaliser cette station d'écoute, nous avons utilisé une combinaison de matériel radio et de logiciels de traitement du signal.

### 🔌 Matériel (Hardware)
* **Récepteur SDR :** Clé USB **RTL-SDR (RTL2832)** faisant office de démodulateur radio.
* **Antenne :** Antenne de type **Hélicoïdale** (polaire circulaire), adaptée à la fréquence de 137 MHz.
* **Connectique :** Câbles coaxiaux et connecteurs de type N.

### 💻 Logiciels (Software)
* **Orbitron :** Pour le *tracking* satellite (prédiction des passages et calcul de l'effet Doppler).
* **SDRSharp :** Pour la réception, la démodulation (FM Large) et l'enregistrement du signal audio.
* **WXtoImg :** Pour le décodage du signal audio en image météo.
* **SatDump :** Outil alternatif pour le traitement des données brutes.

---

## ⚖️ Bilan Technique : Réussites et Difficultés

Ce projet a été marqué par une forte composante de diagnostic matériel avant la phase logicielle.

### ⚠️ Difficultés Rencontrées
1.  **État du matériel :** L'antenne disponible était défectueuse.
    * *Problème :* Le connecteur était cassé et la tête de l'antenne endommagée.
    * *Solution :* Nous avons dû effectuer des réparations manuelles (soudures, remplacement de la connectique) pour restaurer la continuité du signal.
2.  **Qualité de réception :** Malgré la réparation, le signal reçu restait bruité.
3.  **Décodage des images :** Les images obtenues ne couvraient pas la zone espérée (Océan Indien). Nous avons émis l'hypothèse que cela provenait soit de la vétusté de l'antenne (gain insuffisant), soit d'un décalage temporel dans les données reçues.

### ✅ Réussites
* **Réparation réussie :** Remise en état fonctionnel de l'antenne hélicoïdale.
* **Chaîne logicielle fonctionnelle :** Configuration correcte de l'ensemble des logiciels (synchronisation Orbitron/SDRSharp).
* **Acquisition :** Nous avons réussi à capter des signaux et à générer des images, validant le principe technique de la chaîne de réception.

---

## 💡 Ce que ce projet m'a apporté

Ce projet a dépassé le simple cadre logiciel pour toucher à la réalité physique des télécommunications :

* **Compétences Hardware :** J'ai appris à diagnostiquer une panne physique sur une installation radio et à effectuer des réparations (soudures de précision).
* **Compréhension RF :** Meilleure appréhension de l'importance critique de l'antenne (type, état, gain) dans la chaîne de liaison.
* **Traitement du signal :** Découverte concrète du fonctionnement de la Radio Logicielle (SDR) et du décodage de protocoles satellitaires (APT).
* **Persévérance :** Comprendre que le résultat ne dépend pas uniquement de la configuration logicielle, mais de l'intégrité de toute la chaîne physique.
