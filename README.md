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

### [ 01 ] Media & projects — one source, every trial

Load your media, organize encoding experiments, and return to any previous configuration. Each trial keeps its own settings and available quality scores, making comparisons reproducible rather than anecdotal.

<img width="2445" height="1466" alt="project_feature" src="https://github.com/user-attachments/assets/6a48915b-c48d-4700-93e0-2fac594eea5b" />

### [ 02 ] Crop — inspect every border, pixel by pixel

Four magnified trapezoid views expose all frame edges simultaneously, up to **32×**. Detect black bars, inspect average or peak edge values, adjust margins precisely, and watch aspect-ratio information update live.

<img width="2188" height="1309" alt="crop_feature" src="https://github.com/user-attachments/assets/5dbd8d3f-9f02-4299-a039-bc9a52545934" />

### [ 03 ] Resize — choose the right scaler, not just a resolution

Explore **17 scaling methods** across swscale, zimg, and libplacebo, including EWA-family filters and neural options. Compare measured characteristics such as sharpness, ringing, aliasing, and texture; inspect results at pixel level with a source/output slider.

<img width="2188" height="1238" alt="resize_feature" src="https://github.com/user-attachments/assets/cb29782c-d478-476f-ace8-ba6e5bc54222" />

### [ 04 ] Refine — an AI finishing pass, on your terms

**Unleash the next generation of AI-powered video enhancement with NVIDIA SoL**, a groundbreaking new Stable Diffusion model designed specifically for video!

Go beyond traditional upscaling with AI-driven refinement, seamlessly blend the enhanced result with your favorite scaler, and fine-tune noise, seeds, temporal windows, and overlap for precise control. Compare the original and AI-refined output side by side to discover just how far this powerful new technology can push visual quality.

<img width="2447" height="1467" alt="refine" src="https://github.com/user-attachments/assets/c059ffef-e993-4880-b3fc-9cf25d13fb39" />

### [ 05 ] Chroma — color science, made visible

Inspect and control primaries, transfer functions, matrices, chroma siting, and mastering-display information. **CIE 1931 and 1976** diagrams and a saturation timeline keep color decisions grounded in actual data. On a compatible display, the interface can render HDR content in HDR.

<img width="2187" height="1306" alt="image" src="https://github.com/user-attachments/assets/618b5c40-1935-4684-8eb8-72c6f10ad808" />

### [ 06 ] Luma — every nit, accounted for

Analyze HDR luminance on a **0.1–10,000 nit logarithmic waveform**. Track per-frame MaxCLL/MaxFALL, P10–P90 spread, and scene changes; derive metadata from measured, percentile, trimmed, or custom values.

<img width="2445" height="1467" alt="luma_feature" src="https://github.com/user-attachments/assets/6fda9bd0-b9f0-4a36-b92d-b11ec022c0ee" />

### [ 07 ] Encoder — deep control without command-line archaeology

Tune rate control, GOP structure, motion search, lookahead, reference frames, tiles, filters, and more. Start from sensible templates or saved profiles; contextual guidance explains controls and prevents incompatible combinations. The generated command remains accessible.

<img width="2186" height="1307" alt="encoder_feature" src="https://github.com/user-attachments/assets/412c0d89-6fbc-4772-a5a1-559faee210b5" />

### [ 08 ] Quality — seven perspectives, one timeline

Compare **VMAF · SSIM · PSNR · Y-PSNR · HDR-VDP-2 · HDR-VDP-3 · ICtCp ΔE** with per-frame curves and a quality heatmap. Jump directly from a dip in the graph to the corresponding frame. Optional CUDA acceleration helps with FFT-intensive HDR-VDP analysis.

<img width="2186" height="1308" alt="quality_feature" src="https://github.com/user-attachments/assets/afb85e72-21a2-4cc8-a6b2-e97b75f83131" />

### [ 09 ] Metadata — let your file remember the experiment

Attach available quality measurements, thumbnails, HDR statistics, encode settings, and supported Topaz metadata to MKV files for later inspection. Integrity-checked binary analysis data keeps detailed results compact. Compatible **AV1 NVENC** workflows can preserve HDR10+ and Dolby Vision dynamic metadata.

<!-- SCREENSHOT 09: screenshots/09-metadata.png
![Metadata — persistent analysis and HDR metadata](screenshots/09-metadata.png)
-->

### [ 10 ] Monitor — your hardware, under the microscope

See CPU topology, CCDs, cores, L3 cache, individual clocks and temperatures, plus GPU and VRAM information. Control encoder CPU affinity from a live hardware view—no separate monitoring dashboard required.

<!-- SCREENSHOT 10: screenshots/10-monitor.png
![Monitor — live CPU and GPU telemetry](screenshots/10-monitor.png)
-->

### [ 11 ] Settings — the toolchain, taken care of

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

