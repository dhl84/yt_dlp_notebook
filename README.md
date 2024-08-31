# YouTube Downloader

This Python-based YouTube downloader is a versatile tool designed to download videos, playlists, and entire channels from YouTube. It uses the `yt-dlp` library and provides an interactive Jupyter notebook interface for ease of use.

## Features

- Download single YouTube videos, playlists, and channel videos
- Select video quality (including best available and VR/360 videos)
- Interactive user interface using Jupyter widgets
- Supports authentication using browser cookies
- Manage multiple YouTube logins
- Automatic retry mechanism for failed downloads
- Logging system for tracking operations and troubleshooting
- Graceful shutdown and cleanup processes
- FFmpeg integration for highest quality downloads and VR video processing

## Requirements

- Python 3.6+
- Jupyter Notebook
- yt-dlp
- ipywidgets
- browser-cookie3
- ffmpeg-python
- FFmpeg (required for VR video processing and high-quality downloads)

## Setup

1. Ensure you have Python and Jupyter Notebook installed.

2. Install the required Python packages:
   ```
   pip install yt-dlp ipywidgets browser-cookie3 ffmpeg-python
   ```

3. Install FFmpeg:
   - On macOS with Homebrew: `brew install ffmpeg`
   - On Windows: Download from the official FFmpeg website and add to PATH
   - On Linux: Use your distribution's package manager (e.g., `sudo apt-get install ffmpeg`)

4. Copy the provided code into a Jupyter notebook.

## Usage

1. Run the Jupyter notebook containing the code.

2. Execute the cell containing the function definitions.

3. Run the `run_youtube_downloader()` function to start the interactive interface:
   ```python
   run_youtube_downloader()
   ```

4. The interface consists of four tabs:

### Download Video Tab

1. Paste the YouTube URL (video, playlist, or channel) into the URL field.
2. Select the desired quality from the dropdown menu.
3. Choose a login profile if needed (or use "No login").
4. Click the "Download" button to start the download process.

Example:
```python
# To download a video in 1080p quality
url = "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
quality = "1080p"
login = "MyYouTubeAccount"  # or "No login" if not required
```

### Manage Logins Tab

- View saved login profiles
- Delete existing login profiles

### Add Login Tab

1. Select your browser from the dropdown menu.
2. Enter a name for the login profile.
3. Click "Get Cookies" to fetch and save the cookies for the selected browser.

Example:
```python
# To add a new login profile
browser = "chrome"
login_name = "MyYouTubeAccount"
```

### Log Tab

- View the log output for troubleshooting and tracking operations

## Advanced Features

### VR/360 Video Download

The downloader can detect and process VR/360 videos. When a VR video is detected or forced:

1. The video is downloaded in the best available quality.
2. FFmpeg is used to convert the video to a spatial video format compatible with Quest 3 and iOS devices.
3. The converted video is saved with `_spatial` appended to the filename.

Example:
```python
# To force VR processing for a video
url = "https://www.youtube.com/watch?v=VR_VIDEO_ID"
quality = "vr"
```

### Automatic Retry

The downloader will automatically retry failed downloads up to 3 times with increasing delays between attempts.

### Graceful Shutdown

The application implements a graceful shutdown process, ensuring that ongoing operations are properly closed and resources are released.

## Important Notes

- Downloading content from YouTube may be against YouTube's Terms of Service. Use this tool responsibly and only for content you have permission to download.
- Downloading entire channels or large playlists can take a significant amount of time and storage space. Ensure you have sufficient free disk space before starting large downloads.
- The tool uses your browser's cookies for authentication. Make sure you're logged into YouTube in your chosen browser if you want to access content that requires authentication.
- VR video processing requires FFmpeg to be installed and properly configured.
- This tool is for educational purposes only. The user is responsible for complying with all applicable laws and terms of service.

## Troubleshooting

- If downloads fail, check the Log tab for detailed error messages.
- Ensure you have the latest version of the script and all required libraries installed.
- For issues with VR video processing, check that FFmpeg is properly installed and accessible from the command line.
- If you encounter persistent issues with a specific video or channel, try using a different login profile or the "No login" option.

## Disclaimer

This tool is provided as-is, without any warranties or guarantees. The developers are not responsible for any misuse of this tool or any violations of YouTube's Terms of Service.