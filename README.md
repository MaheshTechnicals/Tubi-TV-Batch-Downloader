# 📺 Tubi TV Batch Downloader (Google Colab)

A **Google Colab–based Python script** that allows you to **batch download movies or TV show episodes from Tubi TV** directly into **Google Drive** using `yt-dlp`.

This script supports **episode listing, range-based selection, parallel downloads**, and automatic upload to Google Drive.

---

## 🚀 Features

- Runs entirely on **Google Colab** (no local setup required)
- Saves downloaded files directly to **Google Drive**
- Automatically detects **show or playlist title**
- Lists all available episodes before downloading
- Allows **custom range selection** (example: `1-10`)
- Supports **parallel downloads** (5 at a time by default)
- Downloads best available **video + audio**
- Automatically merges output into **MP4 format**
- Clean and minimal progress output

---

## 🛠 Requirements

You only need:

- A Google account
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

## 📂 Output Directory Structure

Files are saved in Google Drive using the following structure:

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

## 🧑‍💻 How to Use

### 1️⃣ Open Google Colab
Visit:  
https://colab.research.google.com

---

### 2️⃣ Create a New Notebook
- Click **New Notebook**
- Ensure runtime is set to **Python 3**

---

### 3️⃣ Paste the Script
Copy the Python script from this repository and paste it into **a single code cell**.

---

### 4️⃣ Run the Cell
- Execute the cell
- Grant permission when Google Drive asks to mount

---

### 5️⃣ Enter Tubi URL
When prompted:

```
Paste Tubi Link:
```

Example:
```
https://tubitv.com/series/300009876/example-show
```

---

### 6️⃣ Select Episode Range
The script lists all available episodes:

```
1. Episode One
2. Episode Two
3. Episode Three
```

Enter the desired range:
```
1-10
```

---

### 7️⃣ Download Starts 🚀
- Up to 5 downloads run in parallel
- Files are uploaded directly to Google Drive
- Completion message appears when done

---

## ⚙️ Configuration

You can edit these values in the script:

```python
save_path_base = "/content/drive/MyDrive/TubiShows"
ThreadPoolExecutor(max_workers=5)
```

- Reduce `max_workers` if you encounter errors
- Change `save_path_base` to customize the Drive folder

---

## ⚠️ Limitations

- DRM-protected Tubi content cannot be downloaded
- Live streams are not supported
- Excessive parallel downloads may trigger temporary throttling
- Google Colab sessions may disconnect after long inactivity

---

## 🧩 Troubleshooting

**Google Drive not mounting?**  
Re-run the cell and reauthorize Drive.

**Some downloads fail?**  
Lower parallel workers:
```python
ThreadPoolExecutor(max_workers=3)
```

**Show name not detected?**  
Manual input will be requested — this is expected behavior.

---

## 📜 Legal Disclaimer

This project is intended **for educational and personal use only**.

- Do NOT redistribute copyrighted material
- Follow **Tubi TV’s Terms of Service**
- The author is not responsible for misuse

Support content creators whenever possible.

---

## ⭐ Contributing

Contributions are welcome.

Possible improvements:
- Resume interrupted downloads
- Season/Episode auto-naming (S01E01)
- Quality selection
- Subtitle support
- One-click Colab launcher

---

## 👤 Author

**Mahesh Varma**

If you found this project useful, consider giving the repository a ⭐
