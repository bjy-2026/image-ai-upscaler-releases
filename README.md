# Upscaler

A free, personal, non-commercial AI image upscaler for Windows. It enlarges photos 2× to 6× (or to any size)
with AI models that run on your own graphics card. Optional extras clean up JPEG artefacts and noise and enhance
faces, and an opt-in generative mode rebuilds very small or damaged photos.

**Download:** the installer is under [Releases](../../releases/latest).

## Requirements

- Windows 10 (version 2004) or Windows 11, 64-bit.
- An **NVIDIA graphics card** with driver **570 or newer**. About 8 GB of graphics memory or more is
  recommended. Without an NVIDIA card the app still works, but on the processor, which is very slow.
- About 6 GB of free disk space, plus space for any extra AI models you download later.

Everything else is included: .NET, Python, PyTorch with CUDA, the Visual C++ runtime, ExifTool and a starter AI
model. No other installs are needed, and the app works offline right after installation.

## Installing

1. Download `Upscaler-<version>-setup.exe` from the latest release (about 1.9 GB).
2. Run it. It installs for your user account only, into `%LOCALAPPDATA%\Programs\Upscaler`, and doesn't need
   administrator rights.
3. **Windows may show "Windows protected your PC".** The installer isn't code-signed, so Windows doesn't
   recognise the publisher. Click **More info**, then **Run anyway**.

To uninstall, use Settings → Apps → Installed apps → Upscaler. It asks whether to also delete your settings and
downloaded models.

## Checking your download (optional)

Each release includes a `SHA256SUMS` file. To confirm your download is exactly the published file, run this in
PowerShell in your Downloads folder and compare the result with the line in `SHA256SUMS`:

```powershell
Get-FileHash .\Upscaler-0.6.0-setup.exe
```

## Privacy

This app works entirely on your own computer. Your photos, results, settings and logs are never uploaded or sent
to anyone: not the app's author, not the AI model creators, not any cloud service. The AI runs on your own
graphics card. The app has no accounts, no telemetry and no analytics.

The app only goes online when you use the Model Manager to download a model or check for updates. Those requests
download files from GitHub or Hugging Face. They never include your images or any personal information, though,
as with any download, those sites can see your IP address.

## Licences

Upscaler includes third-party software, including PyTorch, NVIDIA CUDA libraries, .NET and ExifTool, and AI models
under their own licences. They are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md); the full texts are
in the `LICENSE-NOTICES` folder of the installed program. NVIDIA, the model authors and the other projects do
not endorse this app. Some optional models offered in the app's Model Manager are for non-commercial use only;
their licence is shown before they are downloaded.

This repository holds release downloads only.
