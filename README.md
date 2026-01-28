# 📺 Tubi TV Batch Downloader (Google Colab)

A **Google Colab–based Python notebook** that allows you to **batch download movies or TV show episodes from Tubi TV** directly into **Google Drive** using **yt-dlp**.

This repository contains a ready-to-use **Jupyter Notebook (`TD.ipynb`)** designed specifically for Google Colab, with episode listing, range selection, and parallel downloads.

---

## 🚀 Features

- ✅ Runs entirely on **Google Colab** (no local setup required)
- 📁 Saves downloaded files directly to **Google Drive**
- 🎬 Automatically detects **show / playlist title**
- 📜 Lists all available episodes before downloading
- 🔢 Allows **custom range selection** (example: `1-10`)
- ⚡ Supports **parallel downloads** (5 at a time by default)
- 🎧 Downloads best available **video + audio**
- 📦 Automatically merges output into **MP4 format**
- 🧼 Clean and minimal progress output

---

## 📁 Repository Contents

```
Tubi-TV-Batch-Downloader/
├── TD.ipynb        # Main Google Colab notebook
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

---

## 🛠 Requirements

You only need:

- A **Google account**
- Access to **Google Colab**
- Stable internet connection

All required Python packages are installed automatically inside Colab.

---

## 📦 Tools & Libraries Used

- Python 3
- yt-dlp
- Google Colab
- Google Drive
- subprocess
- concurrent.futures.ThreadPoolExecutor

---

## ▶️ How to Use (Recommended)

### 1️⃣ Open the Notebook in Google Colab

Upload `TD.ipynb` to Google Colab  
**OR**  
Open Colab → Upload Notebook → Select `TD.ipynb`

---

### 2️⃣ Run the Notebook

- Run the single main cell
- Authorize **Google Drive** when prompted

---

### 3️⃣ Paste the Tubi URL

When asked:

```
Paste Tubi Link:
```

Example:
```
https://tubitv.com/series/300009876/example-show
```

---

### 4️⃣ Select Episode Range

The notebook will list episodes like:

```
1. Episode One
2. Episode Two
3. Episode Three
```

Enter your desired range:

```
1-10
```

---

### 5️⃣ Download Starts 🚀

- Downloads run **in parallel**
- Files are saved automatically to Google Drive
- Final success message appears when complete

---

## 📂 Output Directory Structure

Downloaded files are saved to Google Drive as:

```
Google Drive/
└── MyDrive/
    └── TubiShows/
        └── Show Name/
            ├── Episode 1.mp4
            ├── Episode 2.mp4
            └── ...
```

---

## ⚙️ Configuration (Optional)

You may edit these values inside the notebook:

```python
save_path_base = "/content/drive/MyDrive/TubiShows"
ThreadPoolExecutor(max_workers=5)
```

- Reduce `max_workers` if downloads fail
- Change `save_path_base` to customize storage location

---

## ⚠️ Limitations

- ❌ DRM-protected Tubi content cannot be downloaded
- ❌ Live streams are not supported
- ⚠️ Too many parallel downloads may cause temporary throttling
- ⚠️ Google Colab sessions may disconnect if idle too long

---

## 🧩 Troubleshooting

**Drive not mounting?**  
Re-run the notebook cell and reauthorize Drive.

**Some episodes fail?**  
Lower parallel workers:
```python
ThreadPoolExecutor(max_workers=3)
```

**Show name not detected?**  
Manual input will be requested — this is expected for some playlists.

---

## 📜 Legal Disclaimer

This project is intended **for educational and personal use only**.

- Do **NOT** redistribute downloaded content
- Follow **Tubi TV’s Terms of Service**
- The author is **not responsible for misuse**

Please support original content creators.

---

## ⭐ Contributing

Pull requests are welcome.

Ideas for improvements:
- Resume interrupted downloads
- Season / Episode auto-naming (S01E01)
- Quality selection menu
- Subtitle support
- One-click “Open in Colab” badge

---

## 👤 Author

**Mahesh Varma**  
GitHub: https://github.com/MaheshTechnicals

If this project helped you, consider giving the repository a ⭐
