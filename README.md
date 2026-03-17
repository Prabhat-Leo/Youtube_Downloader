# YouTube Video Downloader (Python)

This is a simple Python script that allows you to download YouTube videos using the **yt_dlp** library.

---

## Requirements

- Python 3.x
- yt_dlp library

Install yt_dlp using:

```bash
pip install yt_dlp
```
## Usage

1.Run the script:

```bash
python youtube_downloader.py
```

2.Enter a valid YouTube video link when prompted.

3.The highest resolution video will be downloaded to your current directory.

## Script Contents

```bash
import yt_dlp

url = input("Enter YouTube URL: ")

ydl_opts = {
    'outtmpl': '%(title)s.%(ext)s',
}

with yt_dlp.YoutubeDL(ydl_opts) as ydl:
    ydl.download([url])

print("Download completed!")
```
## Notes
- Some videos may not download due to region restrictions or YouTube-side issues.
- Ensure your network connection is stable during the download.
