# ♫ Music Bingo — Song Manager & Card Generator

A lightweight, browser-based Music Bingo hosting tool and custom Bingo card generator. Load a local folder of MP3 files, manage your game playlist with automatic ID3 tag reading, shuffle tracks during live events, and generate printable or mobile-shareable Bingo cards via QR codes.

🔗 **Live Demo:** [https://richardtruong0123.github.io/MusicBingo/](https://richardtruong0123.github.io/MusicBingo/)

---

## ✨ Features & Capabilities

### 🎵 Song Manager & Live Player
* **Local Folder Loading:** Import an entire folder of `.mp3` files directly into your browser without uploading files to any external server.
* **Automatic ID3 Tag Parsing:** Uses `jsmediatags` to read embedded MP3 metadata and display tracks cleanly as **`Title — Artist`** (with automatic fallback to cleaned filenames if tags are missing).
* **Shuffle & Play:** Randomly selects a track from your available pool, starts playing it immediately, and moves it to your **Selected / Played** list so you never call the same song twice.
* **Live Search & List Management:** Quickly filter available songs, move tracks manually between *Available* and *Selected* lists, or export your played tracklist to a `.txt` file for record-keeping and verification.

### 🎲 Bingo Card Generator
* **Flexible Grid Sizes:** Generate **$3 \times 3$**, **$4 \times 4$**, or standard **$5 \times 5$** Bingo cards.
* **Custom Pool Selection:** Build cards from **All Loaded MP3s**, **Only Available Songs**, or **Only Selected Songs**.
* **Custom Branding & Free Space:** Personalize the card header title and toggle the center **FREE SPACE (`★`)** on odd-sized grids.
* **Batch Generation:** Create up to 50 randomized, unique cards at once.

### 📱 Digital QR Sharing & Print Support
* **Individual QR Codes & Direct Links:** Every generated card includes a **Share QR / Link** button. Players can scan the QR code with their smartphone camera to open an interactive, standalone digital version of their card and tap squares as songs are called.
* **Print-Ready Layout:** Built-in `@media print` styling strips away the host controls and formats cards cleanly onto pages for physical printing.

### 🔒 Privacy First
* **100% Client-Side Execution:** All audio playback, ID3 tag reading, card generation, and QR code encoding happen locally inside your web browser. Your MP3 files never leave your computer.

---

## 🚀 How to Use

1. **Open the App:** Visit [https://richardtruong0123.github.io/MusicBingo/](https://richardtruong0123.github.io/MusicBingo/).
2. **Load Your Music:** Click **Choose MP3 Folder** and select a directory containing your MP3 tracks.
3. **Generate Cards:**
   * Switch to the **Bingo Cards Generator** tab (or scroll to the generator section).
   * Choose your **Grid Size**, **Quantity of Cards**, **Song Pool Source**, and **Header Title**.
   * Click **Generate Cards**.
   * Either click **Print Cards** for physical copies or click **Share QR / Link** on individual cards for mobile players.
4. **Host the Game:**
   * Switch back to the **Song Manager & Player** tab.
   * Click **🔀 Shuffle & Play** to randomly call and play songs one by one.
   * Played songs automatically move to the **Selected / Played Songs** column so you can verify winning Bingo cards at any time.

---

## 🛠️ Built With
* **HTML5 / CSS3 / Vanilla JavaScript** (Single-file architecture)
* [jsmediatags](https://github.com/aadsm/jsmediatags) — Client-side ID3 metadata reader
* [QRCode.js](https://github.com/davidshimjs/qrcodejs) — Client-side QR code generator
