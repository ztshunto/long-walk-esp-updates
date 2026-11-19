# Step RPG board updates

Ready-to-install updates for the step-powered dungeon RPG that runs on an
ESP32 board. This repository holds **only the built files**; the game's
source lives elsewhere.

Every version is a [release](../../releases). The newest one is always
under **Latest**.

## Install an update on the board

1. From the newest release, download **`update-<version>.bin`**.
2. Join the board's Wi-Fi network and open `http://192.168.4.1/update`.
   Sign in as `admin` with the board's Wi-Fi password.
3. In **1. Install an update**, choose the file and press **Install**.
   The board installs the game data and the program, then restarts.

Boards on version 0.0.17 or older have an older update page with separate
boxes for the program and the game data. Install the program part once
(from that version's GitHub Actions run, `firmware.bin`); after that, the
one file works.

Read each release's notes first: a version that changes the save format
starts a new character.

## What's in a release

| File | What it is |
|---|---|
| `update-<version>.bin` | The program and the game data in one file, for the update page. |
| `latest.json` | The newest version, its file name, size and SHA-256. A board that checks for updates by itself reads this. |

Releases are published automatically by the game's build when a new
version is finished. Please don't upload files here by hand.
