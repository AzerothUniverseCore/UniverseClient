<div align="center">

# ⚔️ Azeroth Universe - UniverseClient

**Client de jeu public d'Azeroth Universe**

![Build](https://img.shields.io/badge/Build-3.3.9-c8aa6e?style=for-the-badge&labelColor=1c1810)
![Engine](https://img.shields.io/badge/Moteur-TrinityCore%203.3.5a-c8aa6e?style=for-the-badge&labelColor=1c1810)
![License](https://img.shields.io/badge/Licence-Usage%20priv%C3%A9-c8aa6e?style=for-the-badge&labelColor=1c1810)

[Site officiel](https://azeroth-universe.eu) • [Discord](https://azeroth-universe.eu) • [Launchers](https://github.com/AzerothUniverseCore/UniverseUpdater) • [Serveur (source)](https://github.com/AzerothUniverseCore/UniverseEmu)

</div>

---

## 📖 À propos

Ce dépôt héberge le **client de jeu** d'Azeroth Universe (Build 3.3.9), distribué via les [Releases](../../releases) GitHub : client de base, patchs `.MPQ` et fichiers additionnels nécessaires pour jouer sur le serveur.

> ℹ️ Ce dépôt distribue des **fichiers de jeu** (client WoW), pas du code source de serveur. Le moteur serveur (TrinityCore, C++/Lua) se trouve dans [UniverseEmu](https://github.com/AzerothUniverseCore/UniverseEmu).

---

## 🚀 Comment jouer

### Option recommandée : utiliser un launcher

La façon la plus simple d'installer et de maintenir le client à jour est d'utiliser l'un des launchers officiels (dépôt [UniverseUpdater](https://github.com/AzerothUniverseCore/UniverseUpdater)) :

| Plateforme | Outil | Description |
|---|---|---|
| 🪟 Windows | Launcher Azeroth Universe | Launcher complet avec interface graphique |
| 🪟 Windows | Mini Launcher | Alternative légère, sans dépendance externe |
| 🍏 macOS | Updater Azeroth Universe | Installation et mise à jour du client |
| 🚨 Windows | Launcher d'urgence | Solution de secours, téléchargement direct depuis ce dépôt |

Les launchers gèrent automatiquement le téléchargement, la vérification des mises à jour et l'extraction des patchs - aucune manipulation manuelle nécessaire.

### Option manuelle

Si vous préférez installer le client vous-même :

1. Téléchargez `AzerothUniverse.rar` depuis les [Releases](../../releases) et extrayez-le dans le dossier de votre choix
2. Téléchargez chaque patch listé ci-dessous depuis les Releases correspondantes et placez-le dans `Data/` ou `Data/frFR/` selon le cas
3. Téléchargez `Additional.rar` et extrayez-le dans `Data/frFR/`
4. Certains patchs volumineux sont scindés en plusieurs volumes RAR (voir [Patchs multi-parties](#-patchs-multi-parties)) : téléchargez toutes les parties d'un même patch avant de les extraire avec [WinRAR](https://www.win-rar.com/) ou [7-Zip](https://www.7-zip.org/)

Arborescence finale attendue :

```
AzerothUniverse/
├── AzerothUniverse.exe (ou .app selon la plateforme)
├── Data/
│   ├── common.MPQ
│   ├── patch.MPQ
│   ├── patch-2.MPQ
│   ├── ...
│   └── frFR/
│       ├── base-frFR.MPQ
│       ├── patch-frFR.MPQ
│       └── ...
└── realmlist.wtf
```

---

## 🗂️ Contenu des Releases

Chaque fichier du client est publié en tant que Release distincte, dont le **tag correspond au nom du fichier**.

### Patchs - `Data/`

```
common.MPQ, common-2.MPQ, expansion.MPQ, lichking.MPQ,
patch.MPQ, patch-2.MPQ, patch-3.MPQ, patch-4.MPQ,
patch-5.MPQ, patch-6.MPQ, patch-7.MPQ, patch-8.MPQ,
patch-9.MPQ, patch-A.MPQ, patch-B.MPQ, patch-C.MPQ,
patch-D.MPQ, patch-E.MPQ, patch-F.MPQ, patch-I.MPQ,
patch-K.MPQ, patch-N.MPQ, patch-T.MPQ, patch-U.MPQ,
patch-V.MPQ, patch-Y.MPQ, patch-Z.MPQ
```

### Patchs - `Data/frFR/`

```
backup-frFR.MPQ, base-frFR.MPQ, expansion-locale-frFR.MPQ,
expansion-speech-frFR.MPQ, lichking-locale-frFR.MPQ,
lichking-speech-frFR.MPQ, locale-frFR.MPQ, patch-frFR.MPQ,
patch-frFR-2.MPQ, patch-frFR-3.MPQ, patch-frFR-4.MPQ,
patch-frFR-5.MPQ, patch-frFR-6.MPQ, patch-frFR-7.MPQ,
patch-frFR-8.MPQ, patch-frFR-U.MPQ, patch-frFR-X.MPQ,
speech-frFR.MPQ
```

### Archives complémentaires

| Fichier | Destination | Contenu |
|---|---|---|
| `AzerothUniverse.rar` | racine du dossier d'installation | Client de base |
| `Additional.rar` | `Data/frFR/` | Fichiers additionnels |

---

## 📦 Patchs multi-parties

GitHub limite chaque asset de Release à 2 Go. Les patchs qui dépassent cette limite sont donc scindés en plusieurs volumes RAR **au sein de la même Release** :

```
patch-4.MPQ (Release)
├── patch-4.part1.rar
├── patch-4.part2.rar
├── patch-4.part3.rar
├── patch-4.part4.rar
└── patch-4.part5.rar
```

⚠️ Deux conventions de nommage coexistent selon les patchs :
- sans zéro devant : `.part1.rar`, `.part2.rar`, `.part3.rar`...
- zéro-paddé sur 2 chiffres : `.part01.rar`, `.part02.rar`, `.part03.rar`...

Téléchargez **toutes** les parties d'un même patch dans le même dossier, puis extrayez uniquement la première partie (`.part1.rar` ou `.part01.rar`) avec WinRAR ou 7-Zip : les volumes suivants sont reconstitués automatiquement. Le launcher d'urgence gère cette détection et cette extraction automatiquement.

---

## 🔗 Liens utiles

- 🌐 Site officiel : [azeroth-universe.eu](https://azeroth-universe.eu)
- 🚀 Launchers & scripts d'installation : [UniverseUpdater](https://github.com/AzerothUniverseCore/UniverseUpdater)
- ⚙️ Code source du serveur : [UniverseEmu](https://github.com/AzerothUniverseCore/UniverseEmu)

---

## 📄 Licence

Ce contenu est distribué exclusivement pour un usage sur le serveur **Azeroth Universe**. Tous droits réservés.
