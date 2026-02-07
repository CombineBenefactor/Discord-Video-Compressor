# Discord Video Compressor

A simple Windows application that compresses video files to under 10 MB, in order to fit Discord's file size limit. Drag a video onto the `.exe` file and it will automatically create a compressed version in the same folder.

[Download here](https://github.com/CombineBenefactor/Discord-Video-Compressor/releases)

## Features
- Automatically calculates bitrate to maximize quality while staying under 10 MB.
- Works with any video length.
- 2-pass FFmpeg encoding for optimal quality.
- Converts video to 720p and reduces frame rate to 30 FPS for efficient compression.

## Requirements
- Windows
- [FFmpeg](https://www.gyan.dev/ffmpeg/builds/) and [FFprobe](https://www.gyan.dev/ffmpeg/builds/) executables (must be in the same folder as the program)
- .NET 8.0+ Runtime (Optional, look under releases)

## Installation
1. Download the compiled `VideoCompressor.exe` from this repository.
2. Download [FFmpeg](https://www.gyan.dev/ffmpeg/builds/) and [FFprobe](https://www.gyan.dev/ffmpeg/builds/) and place the executables in the same folder as `VideoCompressor.exe`.

## Usage
1. Open the folder containing `VideoCompressor.exe` and FFmpeg/FFprobe.
2. Drag any video file (MP4 recommended) onto `VideoCompressor.exe`.
3. The program will:
   - Check if the video is already under ~9.8 MB. If yes, it skips compression.
   - Calculate the correct bitrate for the video to stay under 10 MB.
   - Perform 2-pass compression using FFmpeg.
   - Output a compressed file with `_compressed` appended to the original filename in the same folder.

## Notes
- Only the compiled `.exe` is provided; the source code is not released.
- The program does **not** bundle FFmpeg due to licensing. Users must download FFmpeg themselves.
- Compression reduces resolution and frame rate; high-motion videos may show slight quality loss.

## License
This project is licensed under the MIT License. FFmpeg is licensed separately under LGPL/GPL; see FFmpeg documentation for details.
