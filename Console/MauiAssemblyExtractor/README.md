# MauiAssemblyExtractor

A .NET command-line tool for extracting and analyzing assemblies from .NET MAUI Android Apk file.

## Overview

MauiAssemblyExtractor is a cross-platform console application designed to extract .NET managed assemblies embedded within Android APK packages created with Microsoft's MAUI framework. MAUI applications bundle .NET assemblies in a proprietary compressed binary format within the `libassembly-store.so` native library. This tool automates the entire extraction process, including:

- APK archive decompression
- ELF binary extraction
- Assembly store format parsing
- LZ4 decompression
- Individual assembly extraction

### Primary Use Cases
- **Reverse Engineering**: Analyze MAUI application code and logic
- **Security Assessment**: Conduct static analysis and vulnerability scanning
- **Debugging**: Extract symbols and assemblies for debugging purposes
- **Build Verification**: Verify build artifacts and assembly integrity
- **Code Analysis**: Perform deep-dive code inspection and architecture analysis


## ✨ Features

### Core Capabilities
✅ **Automated APK Processing** - Seamless extraction of APK contents  
✅ **MAUI Assembly Store Parsing** - Understands the proprietary ABAX format  
✅ **LZ4 Decompression** - Efficiently decompresses embedded assembly data  
✅ **ELF File Analysis** - Extracts and processes native .so libraries  
✅ **Interactive CLI** - User-friendly menu-driven interface  
✅ **Comprehensive Logging** - Detailed operational and error logging  
✅ **Error Handling** - Robust validation and informative error messages  

## Requirements

### System Requirements

- **Operating System**: Windows 10/11, macOS (ARM64), or Linux (x64)
- **.NET Runtime**: .NET 6.0 or higher
- **Architecture**: 
  - Windows: x64
  - macOS: ARM64 (Apple Silicon)
  - Linux: x64

### Prerequisites

Before using MauiAssemblyExtractor, ensure you have:

1. **.NET Runtime** installed on your system
   - Download from: https://dotnet.microsoft.com/download
   - Verify installation: `dotnet --version`

2. **Appropriate permissions** to read MAUI application files and write to output directories

## Installation

### Download

Download the appropriate version for your operating system:

- **Windows**: `1.0.0-beta/Windows/win-x64.zip`
- **macOS**: `1.0.0-beta/MacOS/osx-arm64.zip`
- **Linux**: `1.0.0-beta/Linux/linux-x64.zip`

### Extract and Setup

1. **Extract the downloaded zip file** for your operating system to a desired location

2. **Create ApkFile folder** inside the extracted folder (if it doesn't exist)

3. **Place your APK file** inside the `ApkFile` folder

4. **Run the executable**:
   - **Windows**: Double-click `MauiAssemblyExtractor.exe` or run from command prompt
   - **macOS/Linux**: Make executable with `chmod +x MauiAssemblyExtractor` then run `./MauiAssemblyExtractor`

5. **Follow the console instructions** displayed by the application

The tool will automatically detect and process the APK file from the ApkFile folder.

### Application Menu

Once started, the application displays an interactive menu:

```
MauiAssemblyExtractor - Extracts assemblies from a MAUI APK file
=================================================================

Please select an option:
1. Extract Assemblies from MAUI APK
2. Exit

Enter your choice (1 or 2):
```

## Version Information

- **Current Version**: 1.0.0-beta
- **Release Date**: Beta release
- **Status**: Pre-release - use in production at your own discretion

## Platform-Specific Notes

### Windows
- Requires Windows 10 version 1607 or higher
- May require administrator privileges for certain operations

### macOS
- Designed for Apple Silicon (ARM64) Macs
- For Intel Macs, use Rosetta 2 translation
- May require granting permissions in System Preferences > Security & Privacy

### Linux
- Tested on Ubuntu 20.04+ and other modern distributions
- Requires execute permissions (chmod +x)
- May need `libicu` package installed

## Troubleshooting

### "dotnet: command not found"
- Ensure .NET Runtime is installed and added to your system PATH
- Restart your terminal after installation

### Permission Denied (macOS/Linux)
- Run: `chmod +x MauiAssemblyExtractor`
- Ensure you have read permissions for input files and write permissions for output directory

### Application Won't Run (macOS)
- If macOS blocks the application: System Preferences > Security & Privacy > Allow

## Support

For issues, questions, or contributions, please refer to the main .Net-Tools repository.

## License

Please refer to the main repository for license information.

---

*Part of the .Net-Tools collection - .NET Based Application Tools*
