# Ambermoon for Atari: prebuilt binaries

> Thalion's Amiga role-playing game *Ambermoon* (1993) on the Atari Falcon030 and ST/STE.

*An unofficial fan project. It is not affiliated with Thalion or with the current rights holders.*

<p align="center">
  <img src="https://raw.githubusercontent.com/amberport/ambermoon-atari/main/docs/screenshots/falcon-spannenberg.png" width="24%" alt="Falcon030: the city of Spannenberg in 3D">
  <img src="https://raw.githubusercontent.com/amberport/ambermoon-atari/main/docs/screenshots/st-spannenberg.png" width="24%" alt="ST/STE: the same place">
  <img src="https://raw.githubusercontent.com/amberport/ambermoon-atari/main/docs/screenshots/falcon-lyramion.png" width="24%" alt="Falcon030: the Lyramion islands in 2D">
  <img src="https://raw.githubusercontent.com/amberport/ambermoon-atari/main/docs/screenshots/st-lyramion.png" width="24%" alt="ST/STE: the same place">
  <br>
  <sub>Falcon030 and ST/STE at the same places. More in the <a href="https://github.com/amberport/ambermoon-atari/blob/main/SCREENSHOTS.md">screenshots</a>.</sub>
</p>

This repository holds the **programs only**, ready to run, so that you can play without building the port yourself. The **game files are not included**: you need your own copy of the Amiga version of *Ambermoon*. A small tool on your PC puts it into place.

Source code, documentation and how to build it yourself: [amberport/ambermoon-atari](https://github.com/amberport/ambermoon-atari).

## Quickstart

1. **Download the package** that matches your game files from [Releases](https://github.com/amberport/ambermoon-atari-packages/releases):

   | your game files | package |
   |---|---|
   | 1.01 German (Thalion's disks) | `ambermoon-atari-0.8.5-for-1.01-de.zip` |
   | 1.07 English (Thalion's disks) | `ambermoon-atari-0.8.5-for-1.07-en.zip` |
   | 1.21 German (Pyrdacor) | `ambermoon-atari-0.8.5-for-1.21-de.zip` |
   | 1.21 English (Pyrdacor) | `ambermoon-atari-0.8.5-for-1.21-en.zip` |

2. **Install [Python 3](https://www.python.org)** on your PC, if it is not there yet.

3. **Unpack the zip and run the tool** in a terminal, in the unpacked folder:

   ```text
   python3 install.py PATH_TO_YOUR_GAME_FILES
   ```

   On Windows the command is usually `py` instead of `python3`. The game files may be the zip as downloaded, the disk images (ADF, IPF or DMS) or the folder `Amberfiles`. The tool checks their version and copies them into `ATARI\AMBFILES`; your copy stays as it is.

4. **Copy the folder `ATARI`** to the Atari's hard disk.

5. **Start `ATARI\AMBER.TOS`.** The same folder runs on the Falcon and on the ST, and a saved game from one continues on the other.

Each package fits **exactly one version** of the game files. With another version the game says so at the start and ends after a key.

## What you need

- An **Atari Falcon030**, or an **Atari ST/STE with 4 MB** (target: 8 MHz), and a hard disk.
- A **PC with Python 3** (Linux, macOS or Windows) for the installation.
- **The game files** of one of the versions above. Owners of 1.20 German or 1.21 French: there is no package for them yet. Get 1.21 German or English from [Pyrdacor](https://github.com/Pyrdacor/Ambermoon), or build the port yourself.

## Music

The Falcon plays the game's own music. The ST plays **Big Alec's YM version**, which is not in the package either; without it the ST stays silent. Download the file of the entry [Big Alec: Ambermoon](https://sndh.atari.org/?ID=5364) (`ambermon.snd` or `Ambermoon.sndh`) and put it beside `install.py` before you run the tool. It can also come later:

```text
python3 install.py --ym Ambermoon.sndh
```

Settings, such as `MUSIC=YM` on the Falcon, are in `ATARI\AMBFILES\AMBER.INF`.

## Updating to a new release

Your saved games are in `ATARI\AMBFILES`. Copy the folder `ATARI` from the Atari back to the PC, unpack the new package into a new folder and name the old `ATARI` too:

```text
python3 install.py PATH_TO_YOUR_GAME_FILES --saves PATH_TO_THE_OLD_ATARI
```

The tool takes your saved games and settings from there. Before it replaces anything, it asks and keeps a copy in a folder `saves-DATE-TIME`. Then replace `ATARI` on the Atari with the new one.

## What is new, what does not work yet

- What is new in each release: [release notes](https://github.com/amberport/ambermoon-atari/blob/main/RELEASE-NOTES.md).
- Known limitations: [README of the source repository](https://github.com/amberport/ambermoon-atari#known-limitations).

## Reporting bugs

Open an issue in the [source repository](https://github.com/amberport/ambermoon-atari/issues). Name your machine, TOS, monitor and the first line of `ATARI\AMBFILES\BUILD.TXT`.

## Whose work this is

These programs are not only my work. They contain Thalion's code, assembled from Thalion's source, and parts of Thalion's Amiga programs, including graphics; the versions 1.21 also carry Pyrdacor's work on them. I offer them so that people who cannot build the port themselves can play it on their Ataris.

It is unknown who holds the rights to the games published by Thalion Software. If you can make a credible claim to these rights and do not want these programs offered, open an issue and I will take them down.

No rights are claimed, explicitly or implicitly, except the moral rights of the developers of *Ambermoon*, and of the authors of this port, to be identified as such. This is not a license, and no rights are granted.
