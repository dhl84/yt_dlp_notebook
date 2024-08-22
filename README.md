# YouTube Downloader

This Python-based YouTube downloader is a versatile tool designed to download videos, playlists, and entire channels from YouTube. It uses the `yt-dlp` library and provides an interactive Jupyter notebook interface for ease of use.

## Features

- Download single YouTube videos
- Download entire YouTube playlists
- Download all videos from a YouTube channel
- Select video quality (including best available)
- Interactive user interface using Jupyter widgets
- Supports authentication using browser cookies
- FFmpeg integration for highest quality downloads (when available)

## Requirements

- Python 3.6+
- Jupyter Notebook
- yt-dlp
- ipywidgets
- FFmpeg (optional, but recommended for best quality)

## Setup

1. Ensure you have Python and Jupyter Notebook installed.

2. Install the required Python packages:
   ```
   pip install yt-dlp ipywidgets
   ```

3. (Optional but recommended) Install FFmpeg:
   - On macOS with Homebrew: `brew install ffmpeg`
   - On Windows: Download from the official FFmpeg website
   - On Linux: Use your distribution's package manager

4. Copy the provided code into a Jupyter notebook.

## Usage

1. Run the Jupyter notebook containing the code.

2. Execute the cell containing the function definitions.

3. Run the `login_youtube()` function to authenticate (if needed):
   ```python
   login_youtube()
   ```
   This will prompt you to select your browser and fetch YouTube cookies.

4. Use the `interactive_download()` function to start the downloader:
   ```python
   interactive_download()
   ```

5. In the interactive interface:
   - Paste the YouTube URL (video, playlist, or channel) into the URL field.
   - Optionally, specify the desired quality in the Quality field (e.g., '720p', '1080p', or 'best').
   - Click the "Download" button to start the download process.

## Important Notes

- Downloading content from YouTube may be against YouTube's Terms of Service. Use this tool responsibly and only for content you have permission to download.
- Downloading entire channels or large playlists can take a significant amount of time and storage space. Ensure you have sufficient free disk space before starting large downloads.
- The tool uses your browser's cookies for authentication. Make sure you're logged into YouTube in your chosen browser if you want to access content that requires authentication.
- If FFmpeg is not installed, some high-quality formats may not be available for download.
- This tool is for educational purposes only. The user is responsible for complying with all applicable laws and terms of service.

## Troubleshooting

- If you encounter issues with video quality, ensure FFmpeg is installed and properly configured.
- If downloads fail, check your internet connection and ensure you have the necessary permissions to access the content.
- For channel downloads, if no videos are being saved, make sure you're using the latest version of the script that includes the two-step process for channel downloads.

## Disclaimer

This tool is provided as-is, without any warranties or guarantees. The developers are not responsible for any misuse of this tool or any violations of YouTube's Terms of Service.