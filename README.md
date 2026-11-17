<div align="center">

# Open 3D Viewer Studio

**A free 3D viewer for building models: it opens IFC, Revit, SketchUp, Tekla, Allplan, Archicad, Vertex BD, BTL, DWG/DXF, MicroStation DGN, STEP, IFC5 (IFCX), CityJSON, CityGML, GeoJSON, Shapefile, LandXML, glTF, USD, Rhino, COLLADA, 3MF, AMF, FBX, 3DS, VRML/X3D, OBJ, OFF, STL and PLY models, structural analysis models, and LAS, LAZ, E57, PTS, PTX, PCD and ASCII XYZ point clouds, on the desktop and in the browser.**

### [Download](https://github.com/OpenAEC-Foundation/open-3d-viewer-studio/releases/latest) &nbsp;·&nbsp; [Try in your browser](https://open-3d-viewer.open-aec.com) &nbsp;·&nbsp; [Watch the video](https://www.youtube.com/watch?v=cxHO8M8W2Ow)

</div>

**Open 3D Viewer Studio** is the 3D viewer of the [OpenAEC Foundation](https://github.com/OpenAEC-Foundation). Architects, engineers and builders send each other models in many formats; with this viewer you open any of them without the program that made it. You walk around the model, pick an element and read its properties, measure, cut it open, pull it apart per storey or per element, and save it as IFC.

![A SketchUp model of a house on its plot in the viewer, with the models and layers on the left and the file properties on the right](https://raw.githubusercontent.com/OpenAEC-Foundation/open-bim-suite/main/docs/images/readme/hero.png)

## This repository

This repository holds the releases of the viewer and this page, nothing else.

- **Source code, issues and development:** [OpenAEC-Foundation/open-bim-suite](https://github.com/OpenAEC-Foundation/open-bim-suite).
- **The name in the app:** since version 2026.46.1 the viewer is released as the **Open BIM Suite**, one app that also holds the other OpenAEC BIM products. The installers here are those of the suite: the window says Open BIM Suite, and it opens in the viewer the first time.

## Download

The newest version is on the [releases page](https://github.com/OpenAEC-Foundation/open-3d-viewer-studio/releases/latest).

| Platform | Files |
|----------|-------|
| **Windows 10/11 (x64)** | `_x64-setup.exe` (installs without administrator rights) or `_windows-x64.zip` |
| **macOS 11+** | `_macos-universal.dmg` (Apple silicon and Intel) |
| **Ubuntu, Linux Mint** | `_amd64.deb` (ARM: `_arm64.deb`) |
| **Fedora** | `_x86_64.rpm` (ARM: `_aarch64.rpm`) |
| **Any Linux** | `_amd64.AppImage` or `_linux-x64.tar.gz` (ARM: `_arm64.AppImage` or `_linux-arm64.tar.gz`) |

IFC and Revit files open in the desktop app, not in the browser.

## Without installing

**[Open the browser version](https://open-3d-viewer.open-aec.com)**. Drop a model on the page or choose **Open**. You need a browser with WebGPU: a current Chrome, Edge, Firefox or Safari. Your file stays on your computer; nothing is uploaded.

## Checking a download

Every release has a `SHA256SUMS` file and OpenPGP signatures (`.asc`).

```bash
sha256sum -c SHA256SUMS
```

```bash
gpg --verify SHA256SUMS.asc SHA256SUMS
```

The OpenAEC release key is `13F6D414ADEE4ED4CD09AC60601D86C93C504D29`; its public part is [`docs/openaec-releases.asc`](https://github.com/OpenAEC-Foundation/open-bim-suite/blob/main/docs/openaec-releases.asc) in the source repository. The Windows and macOS packages are signed as well. The files here are the same files as in the release of the source repository: their checksums match.

## License

The viewer is free and open: LGPL-3.0-or-later. No licence fees, no account, no upload. The licence text and the notices of the fonts, icons and libraries it uses are in the [source repository](https://github.com/OpenAEC-Foundation/open-bim-suite/blob/main/LICENSE).
