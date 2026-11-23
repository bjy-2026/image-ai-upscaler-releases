# Upscaler — third-party notices

Upscaler is a free, personal, non-commercial project. It includes the third-party software below, each
under its own licence. The full licence texts are in this `LICENSE-NOTICES` folder: Python packages are
under `python\<package>\`, and the others are named after the component. None of these projects endorses
Upscaler.

## Desktop app

| Component | Version | Licence |
|---|---|---|
| .NET runtime and WPF (Microsoft), bundled self-contained | 10.0 | MIT (`.NET-LICENSE.TXT`, `.NET-THIRD-PARTY-NOTICES.TXT`) |
| CommunityToolkit.Mvvm (.NET Foundation) | 8.4.0 | MIT |
| Serilog, Serilog.Sinks.File | 4.3.0, 7.0.0 | Apache-2.0 |

## Inference runtime

| Component | Version | Licence |
|---|---|---|
| CPython (embeddable package) | 3.12.10 | PSF License (`python\CPython-3.12-LICENSE.txt`) |
| Microsoft Visual C++ runtime (msvcp140, vcruntime140, concrt140 …) | 14.5x | Distributable Code under the Visual Studio licence terms |
| PyTorch, torchvision | 2.10.0+cu128, 0.25.0+cu128 | BSD-3-Clause (`python\torch-*\LICENSE`, `NOTICE`) |
| NVIDIA CUDA 12.8 libraries (cudart, cuBLAS, cuBLASLt, cuFFT, cuRAND, cuSOLVER, cuSPARSE, NVRTC, nvJitLink, NVTX, CUPTI) and cuDNN 9, as shipped inside the PyTorch wheel | 12.8 / 9 | NVIDIA CUDA Toolkit EULA and cuDNN Software License Agreement; see below |
| Intel OpenMP runtime (libiomp5md, libiompstubs5md), unmodified, as shipped inside the PyTorch wheel | — | Intel Simplified Software License: Intel's intel-openmp package says it is "free to use and redistribute" under it. https://www.intel.com/content/www/us/en/developer/articles/license/simplified-software-license.html |
| Spandrel, spandrel-extra-arches (chaiNNer) | 0.4.2, 0.2.0 | MIT. Some architectures carry their own licences; the catalog lists each model's licence. |
| NumPy | 2.2.6 | BSD-3-Clause |
| OpenCV (opencv-python-headless) | 4.11.0.86 | Apache-2.0. The FFmpeg video plugin is **not** included. |
| Pillow | 11.3.0 | MIT-CMU (HPND) |
| tifffile | 2026.10.15 | BSD-3-Clause |
| safetensors, diffusers, huggingface-hub (Hugging Face) | 0.8.0, 0.35.2, 0.36.2 | Apache-2.0 |
| OmegaConf, ANTLR 4 runtime | 2.3.0, 4.9.3 | BSD-3-Clause |
| rotary-embedding-torch, einops | 0.8.9, 0.8.2 | MIT |
| psutil | 7.2.2 | BSD-3-Clause |
| tqdm | 4.70.1 | MPL-2.0 and MIT |
| certifi | 2026.11.20 | MPL-2.0 |
| Other Python dependencies (requests, urllib3, idna, charset-normalizer, regex, PyYAML, filelock, fsspec, sympy, mpmath, networkx, Jinja2, MarkupSafe, packaging, typing_extensions, importlib-metadata, zipp, colorama, setuptools) | see `python\` | MIT, BSD, Apache-2.0, PSF-2.0 or CNRI-Python, as in each folder |

**NVIDIA libraries.** The libraries are redistributed unmodified, as part of the PyTorch package, and are
used only by this application. That is what NVIDIA's distribution terms require: the CUDA EULA §1.1.2 and
Attachment A, and the cuDNN SLA "Distribution" supplement, both permit the runtime libraries "as
incorporated in object code format into a software application". The libraries may be used only on systems
with NVIDIA GPUs. The software is NVIDIA's, and NVIDIA does not sponsor or endorse this application. Three
files in the PyTorch package that the app never loads are left out: `cusolverMg64_11.dll`, which is not on
NVIDIA's redistributable list, `nvperf_host.dll` and `nvrtc64_120_0.alt.dll`.
Licences: https://docs.nvidia.com/cuda/eula/ and https://docs.nvidia.com/deeplearning/cudnn/sla/

## Engine components

| Component | Licence |
|---|---|
| SeedVR2 inference code, vendored from numz/ComfyUI-SeedVR2_VideoUpscaler @ 4490bd1 (based on ByteDance-Seed/SeedVR) | Apache-2.0 (`SeedVR2-code-Apache-2.0.txt`). The precomputed text embeddings `pos_emb.pt` and `neg_emb.pt` are ByteDance's (Apache-2.0). |
| YuNet face detector (OpenCV Zoo, `face_detection_yunet_2023mar.onnx`) | MIT (`YuNet-MIT.txt`) |
| ExifTool 13.64 by Phil Harvey (Windows package by Oliver Betz) | Same terms as Perl: Artistic License or GPL (https://exiftool.org/). It runs as a separate program and is not modified. |

## Bundled model

| Model | Author | Licence |
|---|---|---|
| 4xBHI_dat2_real ("Real-world photo") | Philip Hofmann (Phhofm/models) | CC-BY-4.0. Attribution: "4xBHI_dat2_real by Philip Hofmann (Phhofm)". https://github.com/Phhofm/models/releases/tag/4xBHI_dat2_real |

Models installed later with the Model Manager come with their own licences, shown in the Model Manager and
recorded in each model's `manifest.json`. Some are non-commercial (UltraSharp V2, CodeFormer).
