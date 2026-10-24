<div align="center">

# CHROMASTERING

### Encode. Inspect. Measure. Compare.

**A native Windows lab for serious video encoding, HDR inspection, and quality analysis.**

One source. Six codec families. Seven quality metrics. Every experiment in one place.

<p>
  <img alt="Windows" src="https://img.shields.io/badge/Windows-native-202020?style=for-the-badge&logo=windows11&logoColor=white">
  <img alt="Development status: alpha" src="https://img.shields.io/badge/Status-Alpha-B66A35?style=for-the-badge">
  <img alt="Written in C" src="https://img.shields.io/badge/Pure-C-202020?style=for-the-badge&logo=c&logoColor=white">
  <img alt="HDR-aware" src="https://img.shields.io/badge/HDR-aware-386C43?style=for-the-badge">
</p>

**[Download for Windows](https://github.com/RhoCassiopeiae/Chromastering/releases/latest/download/Chromastering.exe)** · **[Website](https://www.chromastering.app/)** · **[Documentation](https://www.chromastering.app/#docs/getting-started)** · **[Releases](https://github.com/RhoCassiopeiae/Chromastering/releases/latest)**

</div>

---

## The idea

Encoding is easy to start. **Knowing what an encode actually did to your image is the hard part.**

Chromastering brings encoding, pixel-level inspection, colorimetry, HDR analysis, and objective quality measurement into one workflow. Try another codec, change a parameter, revisit an earlier result, and compare it on the *same source frame*—without juggling a dozen disconnected tools.

Built for video enthusiasts, archivists, and codec experimenters who want precise control and measurable results.

> [!NOTE]
> **Windows · Alpha software.** Chromastering is actively developed. Features and requirements may evolve between releases.

## Why Chromastering?

| | What it gives you |
| :--- | :--- |
| **One source, many trials** | Keep codec settings and available quality results together; switch between experiments without losing the context. |
| **Six encoding families** | SVT-AV1, H.266/VVenC, AV2/AVM, AV1 NVENC, ProRes, and FFV1. |
| **Seven quality metrics** | VMAF, SSIM, PSNR, Y-PSNR, HDR-VDP-2, HDR-VDP-3, and ICtCp ΔE. |
| **Real HDR workflow** | PQ-aware display on compatible HDR screens, gamut diagrams, nits-based waveforms, and HDR metadata control. |
| **See the pixels** | Four-edge crop inspection, pixel-exact resize previews, and detailed source-versus-output comparisons. |
| **Native by design** | A compact, pure-C DirectX application. No Electron, Python runtime, or traditional installer. |

## Inside the application

Each part of the workflow has its own view. The screenshot slots below are intentionally left as comments until real captures are added; see [Adding screenshots](#adding-screenshots).

### 01 / Media & projects — one source, every trial

Load your media, organize encoding experiments, and return to any previous configuration. Each trial keeps its own settings and available quality scores, making comparisons reproducible rather than anecdotal.

<!-- SCREENSHOT 01: Save your capture as screenshots/01-media-projects.png and uncomment the next line.
![Media and projects — experiments organized around one source](screenshots/01-media-projects.png)
-->

### 02 / Crop — inspect every border, pixel by pixel

Four magnified trapezoid views expose all frame edges simultaneously, up to **32×**. Detect black bars, inspect average or peak edge values, adjust margins precisely, and watch aspect-ratio information update live.

<!-- SCREENSHOT 02: screenshots/02-crop.png
![Crop — four-edge pixel-level inspection](screenshots/02-crop.png)
-->

### 03 / Resize — choose the right scaler, not just a resolution

Explore **17 scaling methods** across swscale, zimg, and libplacebo, including EWA-family filters and neural options. Compare measured characteristics such as sharpness, ringing, aliasing, and texture; inspect results at pixel level with a source/output slider.

<!-- SCREENSHOT 03: screenshots/03-resize.png
![Resize — filter analysis and pixel-exact comparison](screenshots/03-resize.png)
-->

### 04 / Refine — an AI finishing pass, on your terms

Apply **NVIDIA SoL** after upscaling, blend the refined image with your chosen scaler, and control noise, seeds, temporal windows, and overlap. Compare the input and refined output before deciding whether the extra processing is worthwhile.

<!-- SCREENSHOT 04: screenshots/04-refine.png
![Refine — NVIDIA SoL refinement and before-after preview](screenshots/04-refine.png)
-->

### 05 / Chroma — color science, made visible

Inspect and control primaries, transfer functions, matrices, chroma siting, and mastering-display information. **CIE 1931 and 1976** diagrams and a saturation timeline keep color decisions grounded in actual data. On a compatible display, the interface can render HDR content in HDR.

<!-- SCREENSHOT 05: screenshots/05-chroma.png
![Chroma — gamut plots and colorimetry controls](screenshots/05-chroma.png)
-->

### 06 / Luma — every nit, accounted for

Analyze HDR luminance on a **0.1–10,000 nit logarithmic waveform**. Track per-frame MaxCLL/MaxFALL, P10–P90 spread, and scene changes; derive metadata from measured, percentile, trimmed, or custom values.

<!-- SCREENSHOT 06: screenshots/06-luma.png
![Luma — HDR waveform, scene changes and luminance statistics](screenshots/06-luma.png)
-->

### 07 / Encoder — deep control without command-line archaeology

Tune rate control, GOP structure, motion search, lookahead, reference frames, tiles, filters, and more. Start from sensible templates or saved profiles; contextual guidance explains controls and prevents incompatible combinations. The generated command remains accessible.

<!-- SCREENSHOT 07: screenshots/07-encoder.png
![Encoder — detailed codec controls and profiles](screenshots/07-encoder.png)
-->

### 08 / Quality — seven perspectives, one timeline

Compare **VMAF · SSIM · PSNR · Y-PSNR · HDR-VDP-2 · HDR-VDP-3 · ICtCp ΔE** with per-frame curves and a quality heatmap. Jump directly from a dip in the graph to the corresponding frame. Optional CUDA acceleration helps with FFT-intensive HDR-VDP analysis.

<!-- SCREENSHOT 08: screenshots/08-quality.png
![Quality — seven metrics, per-frame graphs and heatmap](screenshots/08-quality.png)
-->

### 09 / Metadata — let your file remember the experiment

Attach available quality measurements, thumbnails, HDR statistics, encode settings, and supported Topaz metadata to MKV files for later inspection. Integrity-checked binary analysis data keeps detailed results compact. Compatible **AV1 NVENC** workflows can preserve HDR10+ and Dolby Vision dynamic metadata.

<!-- SCREENSHOT 09: screenshots/09-metadata.png
![Metadata — persistent analysis and HDR metadata](screenshots/09-metadata.png)
-->

### 10 / Monitor — your hardware, under the microscope

See CPU topology, CCDs, cores, L3 cache, individual clocks and temperatures, plus GPU and VRAM information. Control encoder CPU affinity from a live hardware view—no separate monitoring dashboard required.

<!-- SCREENSHOT 10: screenshots/10-monitor.png
![Monitor — live CPU and GPU telemetry](screenshots/10-monitor.png)
-->

### 11 / Settings — the toolchain, taken care of

Configure the environment and supporting components from the application. The first-run assistant fetches and verifies the tools you select, so the main executable stays lean.

<!-- SCREENSHOT 11: screenshots/11-settings.png
![Settings — application preferences and tool management](screenshots/11-settings.png)
-->

## Codecs and analysis at a glance

| Encoding path | Technology |
| :--- | :--- |
| AV1, software | SVT-AV1 |
| AV1, NVIDIA hardware | NVEncC / NVENC |
| AV2 | AOMedia AVM reference encoder |
| H.266 / VVC | VVenC |
| Intermediate / editing | Apple ProRes profiles |
| Lossless archival | FFV1 |

The **seven quality measurements** range from conventional fidelity metrics (PSNR, Y-PSNR, SSIM) to perceptual scoring (VMAF), HDR visual-difference prediction (HDR-VDP-2/3), and HDR color difference (ICtCp ΔE). Their strengths differ; Chromastering makes it easier to see where they agree—and where they do not.

## Get started in minutes

1. **[Download `Chromastering.exe`](https://github.com/RhoCassiopeiae/Chromastering/releases/latest/download/Chromastering.exe)** from the latest release.
2. Put it in a **writable folder** and launch it. No installer is needed.
3. Follow the first-run assistant to download and verify the processing components you want.
4. Load a video, inspect the source, adjust crop/resize/color settings, and choose an encoder.
5. Create a trial, analyze the result, and compare it with your next experiment.

Optional components, such as **cuFFT** for supported NVIDIA-accelerated HDR quality analysis, are downloaded separately. Actual hardware acceleration and feature availability depend on your system and selected tools.

**[Read the full getting-started guide →](https://www.chromastering.app/#docs/getting-started)**

## A small executable. A serious toolchain.

Chromastering itself is a **single native Windows executable written in C and rendered with DirectX**. Its processing ecosystem brings together established projects including FFmpeg, SVT-AV1, AVM, VVenC, NVEncC, MKVToolNix, libplacebo, and HDR metadata tools. Required external components are downloaded and verified as needed.

The point is simple: **spend your time experimenting with video, not assembling the toolchain.**

## Feedback, releases & community

Chromastering is an independent, non-commercial project shared with the community. Bug reports, reproducible test cases, suggestions, and informed criticism are welcome.

- **[Latest release](https://github.com/RhoCassiopeiae/Chromastering/releases/latest)** — get the current Windows build.
- **[Documentation](https://www.chromastering.app/#docs/getting-started)** — explore the workflow and individual modules.
- **[Issue tracker](https://github.com/RhoCassiopeiae/Chromastering/issues)** — report bugs or suggest improvements.
- **[Website](https://www.chromastering.app/)** — feature tour, updates, and project information.

If you find the project useful, **give the repository a ⭐**. It helps other enthusiasts discover it.

---

<div align="center">

**Chromastering** — *Measure what matters. See what changed.*

Made with curiosity, for people who care about every frame.

</div>

<!--
ADDING SCREENSHOTS

1. Create the `screenshots/` directory in your GitHub repository.
2. Add one PNG per tab, using the exact paths shown in the SCREENSHOT comments above.
3. For each tab, remove the HTML comment markers around its Markdown image line.
   Alternatively, simply paste that Markdown image line below the relevant paragraph.
4. Recommended: 16:9 images where practical, consistent window size, and minimal empty desktop space.
5. Optional: link thumbnails to full-size images if the README becomes too long.

No broken images are shown until you deliberately enable them.
-->

