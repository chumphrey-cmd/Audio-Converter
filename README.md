# Audio Format Converter

A lightweight command-line tool for converting audio files between popular formats:


| Supported Input/Output Formats |
|---------------------|
| MP3                 |
| WAV                 |
| OGG                 |
| M4A                 |
| FLAC               |
| AAC                |
| WMA                |


## Installation

### 1. Python Setup
```bash
# Clone the repository
git clone [your-repo-url]

# Install required Python packages
pip install -r requirements.txt
```

### 2. Install `ffmpeg` Globally as PowerShell Administrator

#### Windows (Recommended Method)
1. Install Chocolatey package manager:
   - Open PowerShell as Administrator
   - Follow installation instructions from Chocolatey's website [HERE](https://chocolatey.org/install#individual)
   
2. Install FFmpeg using Chocolatey:
```powershell
choco install ffmpeg
```

**NOTE:** FFmpeg must be installed globally, not in a virtual environment. Using FFmpeg in a virtual environment may result in a "Win2 File not found error".

#### Alternative FFmpeg Setup
You can also:
- Add FFmpeg to system PATH, or
- Place ffmpeg.exe in the same directory as the script

## Usage

```bash
python audio-converter.py --input INPUT_FILE --output_format FORMAT [--output OUTPUT_PATH]
```

**Arguments:**
- `--input`: Path to the input audio file
- `--output_format`: Desired output format (mp3, wav, ogg, etc.)
- `--output`: Optional output path (file or directory)

## Examples

Convert MP3 to WAV in the same directory:
```bash
python audio-converter.py --input song.mp3 --output_format wav
```

Convert with specific output path:
```bash
python audio-converter.py --input song.mp3 --output_format flac --output /music/converted/
```