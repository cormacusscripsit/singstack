# SingStack User Guide

SingStack is a collaborative recording app for singers. Each member of your ensemble opens the same shared Google Drive folder, listens to practice tracks, records their part, and uploads it. SingStack automatically aligns and mixes everything together — no DAW, no cables, no studio time required.

---

## Table of Contents

1. [How it works](#how-it-works)
2. [First launch — Profile setup](#first-launch--profile-setup)
3. [Home screen](#home-screen)
4. [Opening or creating a project](#opening-or-creating-a-project)
   - [New Project screen](#new-project-screen)
   - [Open Project screen](#open-project-screen)
5. [Project screen](#project-screen)
   - [Track sections](#track-sections)
   - [Playing the mix](#playing-the-mix)
   - [Adding a track](#adding-a-track)
   - [Project menu (⋮)](#project-menu-)
   - [Practice track menu](#practice-track-menu)
   - [Recorded track menu](#recorded-track-menu)
6. [Recording screen](#recording-screen)
7. [Mix Timeline screen](#mix-timeline-screen)
8. [Settings](#settings)
   - [Settings screen](#settings-screen)
   - [Profile screen](#profile-screen)
   - [Connected Accounts screen](#connected-accounts-screen)
   - [Audio Devices screen](#audio-devices-screen)
   - [Calibration screen](#calibration-screen)
   - [Audio Support screen](#audio-support-screen)
   - [About screen](#about-screen)
9. [File Info screen](#file-info-screen)
10. [Required screenshots](#required-screenshots)

---

## How it works

1. A director or arranger creates a shared Google Drive folder and uploads practice tracks (one per voice part).
2. Each singer opens SingStack, taps **New Project** or **Open Project**, and navigates to that shared folder.
3. SingStack downloads the practice tracks, builds a reference mix, and shows the project screen.
4. The singer puts on their headphones, taps **Record**, and sings their part while listening to the mix.
5. SingStack measures the hardware delay of the singer's device, cross-correlates the recording against the reference mix to find the exact timing offset, and uploads the aligned recording back to the Drive folder.
6. As more singers record, the mix grows richer. Tap play at any time to hear the ensemble so far.

The app works on both Android and iOS. A Google account is required.

---

## First launch — Profile setup

The first time you open SingStack you are taken straight to the **Profile** screen. You cannot skip this step.

| Field | What to enter |
|---|---|
| **Nickname** | Your name as it will appear on your recordings — e.g., *Emily* or *Bass Dave*. |
| **Voice Part** | Choose from the dropdown: Soprano, Alto, Tenor, Baritone, Bass, and subdivisions. |

Tap **Get Started** to save and enter the app. You can change these settings at any time from the home screen.

---

## Home screen

The home screen is the starting point for every session.

**Profile card** — shows your nickname and voice part. Tap it to edit your profile.

**Recent Projects** — a list of projects you have opened before, ordered by most recently used. Each tile shows the project name, how long ago you opened it, and how many singers and tracks it contains. Tap a tile to open it directly.

- Tap the **⋮** (three-dot) icon on a recent project tile to see:
  - **Forget** — removes the project from your recents list. This does not delete anything from Google Drive.

**Music folder button** (bottom right, folder with ♫) — opens a menu with two options:

| Option | What it does |
|---|---|
| **Open Project** | Browse Google Drive and open an existing project folder. |
| **New Project** | Browse Google Drive and create a new project folder. |

**Settings gear** (top right) — opens the Settings screen.

---

## Opening or creating a project

Both flows require you to be signed in to a Google account. If you are not signed in, SingStack will prompt you to sign in before showing the Drive browser.

### New Project screen

Navigate your Google Drive to find where you want the project to live, type a project name (a random name is pre-filled — feel free to change it), and tap **Create**.

- **Breadcrumb trail** at the top shows your current location. Tap any crumb to jump back to that level.
- **Home icon** (app bar, top right) — returns to the My Drive root.
- **+ icon** (breadcrumb row, right) — creates a new folder inside the current location.
- The bottom bar always shows which folder the project will be created in.
- Tap **Cancel** to go back without creating anything.

SingStack creates a folder with your chosen name and immediately opens it as a new project.

### Open Project screen

Navigate Google Drive the same way — folders appear in blue, audio files in purple (dimmed, not selectable). Tap a folder to open it as a project.

Your last-used Drive location is remembered and restored automatically on the next visit.

---

## Project screen

The project screen is where you spend most of your time. It shows all the tracks in the current project, a play button for the mix, and controls for adding new recordings.

### Track sections

Tracks are grouped into three collapsible sections. Tap a section header to expand or collapse it.

| Section | Contains |
|---|---|
| **Practice Tracks** | Reference recordings uploaded by the director — one per voice part. |
| **My Tracks** | Recordings you have made on this device. |
| **Others' Tracks** | Recordings from other singers. |

Each track tile shows:
- **Track name** (voice part + singer nickname)
- **Sync status** — a small badge showing whether the track is checked into the mix and how well it aligned. A green checkmark means it is included; a warning means the alignment confidence was low.
- **Duration**

When a Drive project is first opened, SingStack syncs automatically: it downloads any new files and decodes them to WAV. A progress bar shows download and decode progress.

### Playing the mix

The **play/pause button** in the bottom bar builds and plays the current mix (all checked tracks, sync-aligned). Tap again to stop. The button shows a countdown if the mix has a known length.

The mix is rebuilt automatically whenever you change which tracks are included or adjust an offset.

### Adding a track

The **+ button** (bottom right) opens a menu:

| Option | What it does |
|---|---|
| **Record a track** | Opens the Recording screen so you can record a new vocal part. |
| **Add click-in track** | Analyses the mix to detect tempo and prepends a 4-beat click-track count-in. This keeps the ensemble locked to a shared pulse. A dialog lets you confirm the detected BPM before creating the click track. |

### Project menu (⋮)

The three-dot overflow menu in the app bar contains project-level actions:

| Option | What it does |
|---|---|
| **View mix** | Opens the Mix Timeline screen — a horizontal timeline showing all tracks, their waveforms, and detected beat positions. |
| **View files** | Opens the File Info screen — technical details (file size, sample rate, modification date) for every track. |
| **Refresh from Drive** | Checks for new or changed files on Drive and downloads any that are missing locally. Use this after another singer has uploaded a recording. |
| **Reload from Drive** | Clears the local cache and re-downloads all tracks from scratch. Use this if files have become corrupted or if you suspect the local state is out of sync. |

### Practice track menu

Tap the **⋮** next to a practice track to see:

| Option | What it does |
|---|---|
| **Configure** | Opens a dialog to adjust which voice parts this practice track applies to, or to toggle it in/out of the mix. |
| **Delete** | Permanently removes the practice track from the project and from Google Drive (if you own the file). Requires confirmation. |

### Recorded track menu

Tap the **⋮** next to a recorded track (yours or another singer's) to see:

| Option | What it does |
|---|---|
| **Adjust Offset** | Opens a dialog to manually nudge the timing alignment of this track (in milliseconds). Positive values shift the track later; negative values shift it earlier. |
| **Recalculate Offset** | Re-runs the cross-correlation alignment algorithm against the current mix. Useful if new tracks have been added since this track was recorded. |
| **Adjust Volume** | Opens a slider to change the relative volume of this track in the mix. |
| **Delete Track** | Permanently deletes the track from the project and from Google Drive (only available if you own the file). Requires confirmation. |

---

## Recording screen

The recording screen is shown when you tap **Record a track** from the project screen.

**VU meter** — a vertical bar (and floating musical note particles) shows the live microphone input level. If the bar is not moving, check your headset connection or microphone permissions.

**Voice part selector** — a dropdown at the top lets you confirm or change which voice part you are recording before you start.

**Status line** — shows the current state: *Ready to record*, *Opening mic…*, *Recording…*, *Analysing…*.

**Record button** — large button in the centre. Tap once to start recording. While recording:
- An elapsed timer counts up.
- If a mix exists, it plays through your headphones so you can sing along.
- A countdown shows the remaining time if the mix length is known.

**Stop button** — tap to stop recording. SingStack runs the alignment analysis automatically. A results panel appears showing:
- **Offset** — how far your recording was shifted to align with the mix.
- **Confidence** — how well the algorithm matched the two recordings. A higher value means more reliable alignment. Low-confidence results are flagged with a warning.

**Save / Discard** — after reviewing the results, tap **Save** to upload the recording and return to the project screen, or **Discard** to throw it away and try again.

**Calibrate Headset** — if your device has not been calibrated, a button appears here instead of the record button. Calibration measures the hardware audio delay of your specific headset and is strongly recommended for accurate alignment. Tap it to open the Calibration screen inline.

---

## Mix Timeline screen

Accessed from the project menu → **View mix**.

The timeline shows all tracks as horizontal bars arranged on a shared time axis. Each bar displays a waveform visualisation.

- **Scroll horizontally** to move through time.
- **Beat markers** — vertical tick marks overlaid on each track showing detected beat positions. These are used to verify that the ensemble is rhythmically aligned.
- **Playback controls** — play, pause, and stop the mix from within the timeline view.
- The timeline is read-only; edits are made from the project screen.

---

## Settings

Reach the settings screen by tapping the **gear icon** on the home screen.

### Settings screen

A simple list of six items that each open a sub-screen:

| Item | Opens |
|---|---|
| Edit Profile | Profile screen |
| Connected Accounts | Connected Accounts screen |
| Audio Devices | Audio Devices screen |
| Calibration | Calibration screen |
| Audio Support | Audio Support screen |
| About | About screen |

### Profile screen

Change your nickname and voice part. Tap **Save** to update.

### Connected Accounts screen

Shows which Google account is currently signed in (name and email address).

- **Sign Out** — disconnects your Google account from SingStack. You will be asked to sign in again the next time you open or create a project.
- If no account is connected, the screen shows *"Open a project to sign in to Google."*

### Audio Devices screen

Lists the audio input and output devices connected to your phone. Tap a device to select it as the preferred input (microphone) or output (speakers/headphones).

- The list updates automatically when devices are connected or disconnected.
- SingStack uses a priority order (wired headset > Bluetooth > built-in mic/speaker) and selects the best available device by default. Use this screen to override that selection.

### Calibration screen

Calibration measures the end-to-end hardware latency of your headset — the gap between when audio plays out and when the microphone picks it up. This value is used to correct the timing of every recording you make.

**You only need to calibrate once per headset.** If you change headsets, calibrate again.

The calibration flow has four steps:

1. **Intro** — brief explanation. Tap **Next** to continue.
2. **Ready** — put on your headphones and hold the phone steady. Tap **Record** to start.
3. **Active** — the app plays a series of click tones and records the result. Two animated indicators (*Watch!* and *Count!*) show the playback and recording progress.
4. **Results** — shows the measured latency. Tap **Accept & Save** to store it, or **Try Again** to repeat.

If the app cannot detect a clear signal (e.g., headphones are not plugged in), a **No Signal** result is shown with instructions to check the connection.

> **Tip:** Calibration is optional but strongly recommended if you are recording against a mix. Without calibration, the alignment algorithm still works, but its search window is wider and the timing correction may be less precise.

### Audio Support screen

A diagnostic screen that lists the audio codecs available on your device, grouped into four categories:

- **Hardware Encoders** — formats your device can encode in hardware (fast, low power).
- **Software Encoders** — formats available via software (slower, more CPU).
- **Hardware Decoders** — formats your device can decode in hardware.
- **Software Decoders** — formats available via software.

This screen is primarily for troubleshooting. If a recording fails to encode or a track fails to decode, the information here can help identify why.

### About screen

Shows the app version number, a short description of SingStack, and the open-source licence notices for the third-party libraries the app uses (JUCE, FFmpeg, Flutter, Firebase, Google Sign-In).

---

## File Info screen

Accessed from the project menu → **View files**.

Shows a card for each track containing:
- **File name**
- **File size**
- **Last modified date**
- **Sample rate** (e.g., 44100 Hz or 48000 Hz)

This is a diagnostic screen — useful for confirming that a track downloaded correctly or for checking the sample rate of a file before re-running alignment.

---

## Required screenshots

The following screenshots are needed to illustrate this guide. All should be taken on a device at its default text size and with a representative project loaded.

| # | Screen / State | What to show |
|---|---|---|
| 1 | **Home screen — empty state** | No recent projects; animated arrow pointing to the music folder button |
| 2 | **Home screen — with recents** | Profile card at top, two or three recent project tiles, music folder button |
| 3 | **Home screen — open menu** | The "Open Project / New Project" popup open over the music folder button |
| 4 | **Recent project tile — ⋮ menu open** | The "Forget" option visible |
| 5 | **New Project screen** | Breadcrumb showing a subfolder, project name field with a name entered, Create button visible |
| 6 | **Open Project screen** | My Drive root with a mix of folders listed |
| 7 | **Project screen — syncing** | Download/decode progress bar visible, at least one track already showing |
| 8 | **Project screen — ready** | All three sections expanded, mix built, play button available |
| 9 | **Project screen — playing** | Play button in active/stop state, countdown timer visible |
| 10 | **Project screen — project menu open** | The four-item overflow menu visible (View mix, View files, Refresh, Reload) |
| 11 | **Project screen — add menu open** | "Record a track" / "Add click-in track" popup over the + button |
| 12 | **Project screen — recorded track menu open** | Adjust Offset / Recalculate Offset / Adjust Volume / Delete Track visible |
| 13 | **Project screen — practice track menu open** | Configure / Delete visible |
| 14 | **Recording screen — ready** | VU meter at rest, Record button, voice part selector, no prior result |
| 15 | **Recording screen — recording** | VU meter active (particles visible), elapsed timer, stop button |
| 16 | **Recording screen — results** | Alignment results panel showing offset and confidence; Save/Discard buttons |
| 17 | **Recording screen — uncalibrated** | "Calibrate Headset" button shown instead of Record |
| 18 | **Mix Timeline screen** | All tracks visible as waveform bars with beat markers; playback controls |
| 19 | **Settings screen** | All six list items visible |
| 20 | **Profile screen — first launch** | "Welcome to SingStack" title, nickname field, voice part dropdown |
| 21 | **Profile screen — editing** | "Profile" title, existing values filled in, Save button |
| 22 | **Connected Accounts screen — signed in** | Google account name and email, Sign Out button |
| 23 | **Connected Accounts screen — signed out** | "No accounts connected" empty state |
| 24 | **Audio Devices screen** | Input and output device lists with at least one wired headset visible |
| 25 | **Calibration screen — intro step** | Intro text and Next button |
| 26 | **Calibration screen — active step** | Watch!/Count! indicators animated, recording in progress |
| 27 | **Calibration screen — results** | Latency value shown, Accept & Save and Try Again buttons |
| 28 | **Audio Support screen** | At least two codec sections populated |
| 29 | **About screen** | Version number visible, licence list partially shown |
| 30 | **File Info screen** | Two or three track cards showing file size, sample rate, modified date |
