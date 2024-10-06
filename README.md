# MFC Video Watermarking Project with GPU Acceleration
Video Encoding Decoding usig FFMPEG

# Project Overview

This MFC-based desktop application reads a video file, decodes it using FFmpeg, applies a watermark to each frame, and re-encodes the video in ASF format. Additionally, it supports GPU acceleration for encoding/decoding using NVIDIA's NVENC technology (CUDA-enabled devices), providing faster processing and improved performance.

# Prerequisites

Before building and running this project, ensure you have the following installed:

    Microsoft Visual Studio: Required for building the MFC application.
    MFC Framework: Ensure that your Visual Studio installation includes the MFC libraries.
    FFmpeg (Version 6.0 or later): FFmpeg is used for video decoding, watermarking, and encoding. Make sure FFmpeg is installed and configured properly.
    OpenCV: Required for image and video frame manipulation (optional, if used for watermarking).
    OpenSSL: Ensure OpenSSL is installed for cryptographic operations (optional, if needed).
    Windows SDK: Required for Windows-based system programming.
    CUDA Toolkit: Required for GPU acceleration. Install the appropriate version for your system.
    NVIDIA GPU with NVENC support: Ensure your system has a supported NVIDIA GPU for GPU-based encoding/decoding.


# Usage Instructions
Step 1: Launch the Application

Run the compiled application from Visual Studio or execute the generated .exe file from the Release or Debug folder.
Step 2: Input Video

    Use the "Browse" button to select the input video file (supports formats like .mp4, .avi, etc.).
    The application will use FFmpeg to decode the video, with optional GPU acceleration if available.

Step 3: Select Encoding/Decoding Mode

    CPU Mode: Decodes and encodes the video using the CPU.
    GPU Mode: Utilizes GPU hardware acceleration for both encoding and decoding if a compatible NVIDIA GPU is available.
        If GPU mode is selected, NVENC will be used for encoding, and CUDA/NVDEC will be used for decoding.

Step 4: Apply Watermark

    The watermark image (watermark.png) will be applied to each frame of the video. You can change the watermark by replacing the watermark.png file in the /resources folder.
    You can adjust the position and transparency of the watermark via the application's GUI.

Step 5: Encode Video

    After watermarking, the application encodes the video in ASF format using FFmpeg.
    If GPU mode is selected, the video will be encoded using NVENC for faster performance.
    Click the "Save" button after select the output location for the encoded video.
