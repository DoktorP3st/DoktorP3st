<div align="center">

# Pestovich

**Python Developer · Music Tooling · AI Tooling · Game Macros · Twitch Streaming**

Outils Windows locaux — rapides, sans serveur, sans abonnement.

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat-square&logo=python&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-0078D4?style=flat-square&logo=windows&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/UI-CustomTkinter-1F6AA5?style=flat-square)
![Claude](https://img.shields.io/badge/Claude-Anthropic-D97706?style=flat-square)
![HTML5](https://img.shields.io/badge/HTML5%20%2F%20CSS3%20%2F%20JS-StreamElements-9146FF?style=flat-square&logo=twitch&logoColor=white)

</div>

---

## Projets

### 🤖 IA Vocal

---

#### [StreamOracle](https://github.com/Pestovich/StreamOracle)

> Assistant IA vocal pour streamers Twitch — wake word, transcription Whisper locale (GPU), réponses Claude, synthèse vocale Microsoft Neural.

```
StreamOracle/
├── app.py               Interface graphique (customtkinter)
├── config.py            Paramètres centralisés
└── core/
    ├── listener.py      Capture micro · VAD RMS · Whisper · wake word
    ├── brain.py         Claude Haiku · system prompt · historique multi-tours
    └── voice.py         edge-tts async · lecture sounddevice
```

**Stack** — `faster-whisper` `anthropic` `edge-tts` `sounddevice` `miniaudio` `customtkinter`

---

### 🎬 Outils musicaux

---

#### [TAC MP4 Studio](https://github.com/Pestovich/TAC-MP4-Studio) `v2.1`

> Génère des vidéos musicales réactives frame by frame, beat by beat — export MP4 HD/vertical, sans cloud.

![Version](https://img.shields.io/badge/version-2.1.0-7c3aed?style=flat-square)
![librosa](https://img.shields.io/badge/librosa-audio%20analysis-FF6B35?style=flat-square)
![FFmpeg](https://img.shields.io/badge/FFmpeg-NVENC%20%2F%20libx264-007808?style=flat-square)

```
TAC-MP4-Studio/
├── main.py                  Point d'entrée
├── requirements.txt
├── app/
│   ├── audio.py             Analyse STFT · onset · RMS · beats
│   ├── renderer.py          Pipeline frame : image · texte · vignette · glow
│   ├── spectrum.py          10 styles de spectre + orbe audio
│   ├── vinyl.py             Disque vinyle VYNLE Studio v2
│   ├── particles.py         Particules · fumée · plasma · lueur
│   ├── exporter.py          Pipeline FFmpeg (NVENC GPU / libx264 CPU)
│   ├── models.py            RenderSettings dataclass
│   ├── presets.py           13 presets visuels + palettes
│   ├── config.py            Persistance JSON (AppData)
│   ├── errors.py            8 exceptions métier typées
│   └── ui/
│       ├── app.py           App — état · lifecycle · éditeur
│       ├── editor.py        Onglets paramètres + callbacks
│       ├── preview.py       Preview live 30 fps + waveform
│       ├── pages.py         Accueil · historique
│       └── widgets.py       Composants réutilisables
```

**Stack** — `numpy` `opencv-python` `Pillow` `librosa` `soundfile` `scipy` `customtkinter` `FFmpeg`

---

#### [TAC Players Music Overlay](https://github.com/Pestovich/TAC-Players-Music-Overlay)

> Lecteur audio Python avec overlay OBS live — pochette, titre, barre de progression animée.

```
TAC-Players-Music-Overlay/
├── main.py                  Lanceur
├── overlay/
│   ├── index.html           Overlay OBS (Browser Source)
│   ├── script.js            Polling JSON + animations
│   └── style.css            Thèmes visuels
└── src/
    ├── core/
    │   ├── config.py        Paramètres utilisateur
    │   └── scanner.py       Détection piste en cours
    ├── player/
    │   ├── engine.py        Moteur de lecture
    │   └── writer.py        Export JSON → overlay
    └── ui/
        └── control.py       Interface de contrôle
```

**Stack** — `Python` `HTML/CSS/JS` `OBS Browser Source`

---

#### [TAC Extract Lyrics](https://github.com/Pestovich/TAC-Extract-Lyrics)

> Explorateur de musique et paroles — multi-sources API, curation swipe, historique et listes de lecture.

```
TAC-Extract-Lyrics/
├── eltac.py                 Point d'entrée
└── src/
    ├── api/                 Deezer · MusicBrainz · ListenBrainz · AudioDB
    ├── core/                Config · errors · logger
    ├── domain/              Models (Track, Lyrics, Playlist)
    ├── services/            Curation · music service
    ├── storage/             JSON store · repositories
    ├── ui/                  Main window · widgets
    └── utils/               Text helpers
```

**Stack** — `customtkinter` `requests` `Deezer API` `MusicBrainz API`

---

### 🎮 Game Macros

---

#### [DiabloIV Macro](https://github.com/Pestovich/DiabloIV-Macro-ByPestovich)

> Overlay automation pour Barbare Tourbillon Diablo IV — cooldowns, maintien WW, potion automatique. 5 langues.

```
DiabloIV-Macro-ByPestovich/
├── ww_barb.py               Moteur macro + overlay Tkinter
├── i18n.py                  Internationalisation
└── locales/                 fr · en · de · es · it
```

**Stack** — `pynput` `tkinter` `winsound` `ctypes`

---

#### [Forza Horizon 6 — Race Loop Macro](https://github.com/Pestovich/ForzaH6-RaceLoop-Macro)

> Boucle de courses automatisée pour Forza Horizon 6 — overlay live avec phases, timer et compteur de tours.

```
ForzaH6-RaceLoop-Macro/
├── forza_race_loop.py       Moteur + overlay Tkinter
└── launch.bat               Lanceur Windows
```

**Stack** — `pynput` `tkinter` `threading` `json`

---

### 📺 Overlays Twitch — StreamElements / OBS

---

#### [Mort-o-Mètre](https://github.com/Pestovich/Mort-o-M-tre) · [BubuRog Die Counter](https://github.com/Pestovich/BubuRog-Die-Counter)

> Compteurs de morts interactifs pour stream Twitch — incrémentation clavier, animations, responsive.

#### [CIPHER](https://github.com/Pestovich/Overlay-Twitch-CIPHER)

> Chat overlay cyberpunk pour StreamElements — scanlines, glow néon, barres de signal, coins en L dans la couleur de chaque viewer.

#### [Chat Overlay](https://github.com/Pestovich/Pestovich-Overlay-Chat-V1)

> Overlay chat Twitch gratuit — design épuré, personnalisable, prêt pour StreamElements.

#### [Cam Overlay 16:9](https://github.com/Pestovich/Pestovich-Overlay-Cam-16x9-V1) · [Cam Overlay 1:1](https://github.com/Pestovich/Pestovich-Overlay-Cam-1x1-V1)

> Cadres caméra format 16:9 et 1:1 — libres d'utilisation, OBS ready.

```
Overlays/
└── HTML + CSS + JS   (StreamElements / Browser Source OBS)
```

---

## Stack technique

| Domaine | Outils |
|---|---|
| **Audio / Vidéo** | `librosa` `soundfile` `scipy` `opencv-python` `Pillow` `FFmpeg` |
| **IA / Vocal** | `anthropic` `faster-whisper` `edge-tts` `sounddevice` `miniaudio` |
| **Interface** | `customtkinter` `tkinter` `tkinterdnd2` |
| **Automation** | `pynput` `ctypes` `threading` `winsound` |
| **Web / Stream** | `HTML5` `CSS3` `JavaScript` `OBS Browser Source` `StreamElements` |
| **Persistance** | `JSON` `AppData` `pathlib` |
| **Plateforme** | `Windows 10 / 11` `Python 3.11+` |

---

<div align="center">

*Tous les projets sont locaux, open source et sans abonnement.*

🎮 [twitch.tv/Pestovich](https://twitch.tv/Pestovich)

</div>
