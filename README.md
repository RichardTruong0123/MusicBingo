# ♫ Music Bingo — Manager, Card Generator, LyricSync & LRC Manager

A feature-rich, browser-based Music Bingo hosting suite, custom Bingo card generator, karaoke lyric synchronizer, and bulk LRC lyric manager. Load local MP3 folders, manage game sessions with automatic ID3 tag reading, sync real-time karaoke lyrics, fetch `.lrc` files from LRCLIB, and generate printable or mobile-shareable Bingo cards via QR codes.

🔗 **Live Demo:** [https://richardtruong0123.github.io/MusicBingo/](https://richardtruong0123.github.io/MusicBingo/)

---

## ✨ Implemented Features & Capabilities

### 🌙 Dark & Light Theme Support
* **Theme Toggle Switch:** Instantly switch between light and dark modes with a dedicated header button.
* **Persistent Preference:** Automatically remembers your theme preference using `localStorage` and respects system color scheme preferences.

### 🎵 Song Manager & Live Player
* **Local Folder Loading:** Import an entire folder of `.mp3` files directly into your browser without uploading files to external servers.
* **Automatic ID3 Tag Parsing:** Uses `jsmediatags` to read embedded MP3 metadata and display tracks cleanly as **`Title — Artist`** (with automatic fallback to cleaned filenames if tags are missing).
* **Shuffle & Play:** Randomly selects a track from your available pool, starts playing it immediately, and moves it to your **Selected / Played** list so you never call the same song twice.
* **Live Search & List Management:** Quickly filter available songs, move tracks manually between *Available* and *Selected* lists, or export your played tracklist to a `.txt` file.

### 🎲 Bingo Card Generator & QR Sharing
* **Flexible Grid Sizes:** Generate **$3 \times 3$**, **$4 \times 4$**, or standard **$5 \times 5$** Bingo cards.
* **Custom Pool Selection:** Build cards from **All Loaded MP3s**, **Only Available Songs**, or **Only Selected Songs**.
* **Custom Branding & Free Space:** Personalize the card header title and toggle the center **FREE SPACE (`★`)** on odd-sized grids.
* **Batch Generation:** Create up to 50 randomized, unique cards at once.
* **Digital QR Sharing & Print Support:** Every card includes a QR code and direct link so players can open interactive digital versions on their phones. Built-in `@media print` styling formats physical cards cleanly for printing.

### 🎤 LyricSync Studio
* **Karaoke Mode & Real-Time Visualizer:** Features an audio analyzer canvas, live seekable progress bar, playback speed controls, and smooth auto-scrolling karaoke lyrics.
* **Lyric Syncer Editor Studio:** Paste plain lyrics and press <kbd>T</kbd> or click **Stamp Current Line** while music plays to stamp exact `[mm:ss.xx]` timing tags and export `.lrc` files.
* **Built-in Synthesizer Demo:** Includes a built-in synthwave demo track and lyric set so you can test LyricSync instantly without loading an MP3 folder.

### 📑 LRC Manager & LRCLIB Bulk Search
* **Automatic `.lrc` Detection:** Automatically detects existing `.lrc` files when loading a local folder and registers them in memory.
* **Bulk LRCLIB Integration:** Searches [LRCLIB](https://lrclib.net/) automatically for missing tracks, intelligently skipping songs that already have local `.lrc` files.
* **Batch & Individual Exports:** Save fetched lyrics directly back to your song folder using the File System Access API or download them in bulk via ZIP.

### 🔒 Privacy First
* **100% Client-Side Execution:** All audio playback, ID3 tag parsing, lyric synchronization, and QR code generation happen locally in your browser.

---

## 💡 Nice to Have (Future Roadmap)

Here are the planned features and enhancements slated for future implementation:

1. **Game Session & Winner Verification (Bingo Card Validator)**
   * Allow hosts to input the exact sequence of called songs and instantly verify whether a player's card (via Card ID or QR scan) contains a valid winning bingo (horizontal, vertical, diagonal, or four corners).
2. **Built-In Streaming Audio Previews (Spotify / YouTube API)**
   * Supplement local MP3 folders with optional streaming audio search integration to preview tracks or fetch missing album artwork on the fly.
3. **Automatic LRC Lyric Timing Adjustment Tool ("Time-Shift")**
   * Provide a quick offset slider ($+ / - 0.5\text{s}$, $+ / - 1.0\text{s}$, etc.) directly in the LyricSync Studio to instantly shift all timestamps forward or backward to compensate for intro silence.
4. **Custom Bingo Card Theme & Color Customizer**
   * Add options in the Bingo Cards Generator to select custom color palettes (e.g., Neon Synthwave, Retro Vinyl, Holiday) and upload event logos for branded printouts.

---

## 🚀 How to Use

1. **Open the App:** Visit [https://richardtruong0123.github.io/MusicBingo/](https://richardtruong0123.github.io/MusicBingo/).
2. **Load Your Music:** Click **Choose MP3 Folder** in the Song Manager tab and select a directory containing your MP3 tracks.
3. **Generate Cards:**
   * Switch to the **Bingo Cards Generator** tab.
   * Choose your **Grid Size**, **Quantity of Cards**, **Song Pool Source**, and **Header Title**.
   * Click **Generate Cards** and either print physical copies or share mobile QR codes.
4. **Host & Sync:**
   * Use **Song Manager** to call songs or send tracks to **LyricSync Studio** for karaoke display.
   * Use **LRC Manager** to automatically find and sync lyrics for your entire library.

---

## 🛠️ Built With
* **HTML5 / CSS3 / Vanilla JavaScript** (Single-file architecture with Tailwind CSS)
* [jsmediatags](https://github.com/aadsm/jsmediatags) — Client-side ID3 metadata reader
* [QRCode.js](https://github.com/davidshimjs/qrcodejs) — Client-side QR code generator
* [JSZip](https://stuk.github.io/jszip/) — Client-side ZIP bundle generator