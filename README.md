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

## File formats

A study of 3D formats in November 2026 listed about 270 formats and format families, spread over 21 industries. The viewer opens 47 of them today. The lists below cover every industry in that study, not only buildings: plant and shipbuilding, mechanical CAD, electronics, games and film, GIS, scanning, 3D printing, medicine, simulation, the subsurface and more.

What the status column means:

- **Opens**: the viewer reads it today.
- **Coming**: a reader is in an open pull request.
- **Next**: the formats being added first.
- **Later**: planned, but more work.
- **Via export**: closed, with no public specification or open reader. The viewer opens the format the program exports; the status names that export.
- **Not planned**: little value for this viewer, or no 3D geometry.

Compressed glTF (Draco, meshopt, KTX2 textures) does not open yet; plain glTF and GLB do.

### Buildings, BIM and coordination

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| IFC 2x3, IFC4, IFC4x3 | .ifc .ifczip | Open | Opens |
| IFC5 (IFCX) | .ifcx | Open | Opens |
| Revit | .rvt .rfa | Closed | Opens |
| Revit templates | .rte .rft | Closed | Later |
| SketchUp | .skp | Closed | Opens |
| Tekla Structures | .db1 .tbp | Closed | Opens |
| Allplan | .ndw | Closed | Opens |
| Archicad | .pln .pla | Closed | Opens |
| Archicad BIMx and templates | .bimx .tpl | Closed | Via export: PLN or IFC |
| Vertex BD | .vxz .vxm | Closed | Opens |
| BTL (timber machining) | .btl .btlx | Open | Opens |
| Vectorworks | .vwx | Closed | Opens |
| DWG | .dwg | Closed | Opens |
| DXF | .dxf | Documented | Opens |
| MicroStation DGN V8 | .dgn | Closed | Opens |
| MicroStation DGN V7 | .dgn | Documented | Later |
| Coordination model | .smc | Closed | Opens |
| BCF issues | .bcfzip .bcf | Open | Opens (in the Validator) |
| Navisworks | .nwd .nwc .nwf | Closed | Via export: IFC or FBX |
| SVF | .svf | Closed | Later |
| SVF2 | folder | Closed | Via export: IFC |
| iModel | .bim | Documented (SQLite) | Later |
| TrimBIM | .trb | Closed | Via export: IFC or Tekla |
| 3MX and 3SM reality meshes | .3mx .3mxb .3sm | 3MX published, 3SM closed | Later |
| gbXML (energy model) | .xml | Open | Later |
| IDS | .ids | Open, no geometry | Not planned |
| COBie | .xlsx | Open, no geometry | Not planned |
| Speckle | server, JSON | Open | Later |

### Infrastructure, roads and rail

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| LandXML | .xml | Open | Opens |
| ASAM OpenDRIVE | .xodr | Open | Next |
| railML 3 | .railml | Open (registration) | Later |
| InfraGML / LandInfra | .gml | Open | Later |
| 12d Model ASCII | .12da | Documented | Later |
| InfraWorks | .sqlite | Closed | Via export: IFC or LandXML |
| KLIC / IMKL (cables and pipes) | .xml .gml in .zip | Open | Later |

### Structural analysis

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| Structural analysis text model | .e2k | Documented text | Opens |
| IFC analysis results | .ifcfemresults | Open | Opens |
| sam-json | .json | Open | Opens |
| SAF (Structural Analysis Format) | .xlsx | Open | Next |
| Structural analysis text model | .s2k .$2k | Documented text | Next |
| Structural analysis command files | .std .mgt | Documented text | Later |
| Structural analysis models, binary | .edb .rtd .esa .rf6 | Closed | Via export: SAF or IFC |
| CIS/2 (steel) | .stp | Open | Later |
| DSTV NC1 (steel CNC) | .nc1 | Open | Later |
| BVBS (rebar shapes) | .abs | Open | Later |

### Plant, process, offshore and shipbuilding

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| AVEVA RVM + ATT | .rvm .att | Closed, reverse-engineered | Later |
| AVEVA E3D / Marine | .dab | Closed | Via export: IFC |
| VUE / ZVF (plant review) | .vue .zvf | Closed | Via export: DGN |
| PDS legacy plant model | .dgn .dri .prp | Closed | Via export: DGN V8 |
| ZGL / XGL | .zgl .xgl | Closed | Later |
| CADMATIC / NUPAS | own, eShare | Closed | Via export: IFC |
| Hull stability geometry | .gf .gft .pm | Closed | Via export: DXF |
| Naval hull design model | .msd | Closed | Via export: 3DM |
| ShipConstructor / Orca3D | .dwg .3dm | Closed | Opens (as DWG or 3DM) |

### Mechanical CAD, PLM, automotive and aerospace

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| STEP | .step .stp .stpz | Open | Opens |
| SolidWorks | .sldprt .sldasm | Closed | Opens |
| Rhino | .3dm | Documented | Opens |
| FreeCAD | .fcstd | Open | Opens |
| Solid Edge | .par .psm .asm | Closed | Coming |
| Inventor | .ipt .iam | Closed | Coming |
| IGES | .igs .iges | Open | Later |
| JT | .jt | Open (paid ISO spec) | Later |
| Parasolid | .x_t .x_b | Semi-open | Later |
| ACIS | .sat .sab .smt | Semi-open | Later |
| Open CASCADE BREP | .brep .xbf | Open | Later |
| 3DXML / CGR | .3dxml .cgr | 3DXML documented, CGR closed | Later |
| CATIA V5 | .catpart .catproduct | Closed | Via export: STEP |
| CATIA V4 | .model | Closed | Via export: STEP |
| NX | .prt | Closed | Via export: STEP |
| Creo / Pro/E | .prt .asm | Closed | Via export: STEP |
| Fusion | .f3d .f3z | Closed | Via export: STEP |
| Alias | .wire | Closed | Via export: STEP or IGES |
| DWF / DWFx | .dwf .dwfx | Toolkit published | Via export: DWG |
| eDrawings | .eprt .easm | Closed | Via export: STEP |
| 3D PDF (U3D, PRC) | .pdf | U3D open, PRC paid spec | Later |
| PLM XML | .plmxml | Documented | Later |
| QIF | .qif | Open | Later |
| VDA-FS | .vda | Open | Later |
| ZW3D | .z3 | Closed | Via export: STEP |
| Kompas-3D | .m3d | Closed | Via export: STEP |
| T-FLEX | .grb | Closed | Via export: STEP |
| Cimatron | .elt | Closed | Via export: STEP |
| SpaceClaim | .scdoc | Closed | Via export: STEP |
| OpenSCAD | .scad | Open script | Not planned |
| CadQuery | .py | Open script | Not planned |

### Electronics (ECAD-MCAD)

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| IPC-2581 | .xml .cvg | Open | Later |
| ODB++ | folder, .tgz | Semi-open | Later |
| IDF 3.0 / 4.0 | .emn .emp .idf | Open | Later |
| IDX (EDMD) | .idx | Documented | Later |
| Gerber X2 / X3 | .gbr | Open | Later |
| KiCad PCB | .kicad_pcb | Open | Via export: STEP or VRML |
| Altium | .pcbdoc | Closed | Via export: STEP |

### CNC and CAM

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| G-code (ISO 6983, RS274) | .nc .gcode .tap .ngc | Open | Next |
| STEP-NC | .stp | Open (paid ISO spec) | Later |
| APT / CL data | .apt .cl .cls | Open | Later |
| Mastercam | .mcam | Closed | Via export: STEP |
| Fusion CAM | in .f3d | Closed | Via export: STEP |

### Games, film, VFX and 3D content

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| glTF | .gltf .glb | Open | Opens |
| USD | .usd .usda .usdc .usdz | Open | Opens |
| FBX | .fbx | Closed | Opens |
| COLLADA | .dae | Open | Opens |
| Blender | .blend | Open | Opens |
| 3DS | .3ds | Documented | Opens |
| OBJ | .obj .mtl | Open | Opens |
| VRML / X3D | .wrl .x3d | Open | Opens |
| Alembic | .abc | Open | Later |
| OpenVDB / NanoVDB | .vdb .nvdb | Open | Later |
| MagicaVoxel | .vox | Open | Next |
| LightWave | .lwo .lws | Open | Later |
| Quake / Source models and levels | .md2 .md3 .md5 .mdl .smd .bsp | Documented | Later |
| DirectX | .x | Documented | Later |
| Ogre | .mesh | Documented | Later |
| Irrlicht | .irr | Documented | Later |
| MilkShape 3D | .ms3d | Documented | Later |
| Blitz3D | .b3d | Documented | Later |
| IQM | .iqm | Open | Later |
| PMX | .pmx | Documented | Later |
| VRM (avatars) | .vrm | Open | Later |
| MaterialX / OpenPBR | .mtlx | Open | Later |
| Houdini | .bgeo .geo .hip | Partly documented | Later |
| Maya | .ma .mb | Closed | Via export: FBX or USD |
| 3ds Max | .max | Closed | Via export: FBX |
| Cinema 4D | .c4d | Closed | Via export: FBX |
| Modo | .lxo | Closed | Via export: FBX |
| ZBrush | .ztl | Closed | Via export: OBJ |
| Unreal assets | .uasset .pak | Closed | Not planned |
| Unity | .prefab .unity | Closed | Not planned |
| Godot | .tscn | Open | Not planned |
| Render scenes (RenderMan, Arnold, POV-Ray, Mitsuba) | .rib .ass .pov .xml | Partly open | Not planned |
| Substance | .sbsar | Closed | Not planned |
| SpeedTree | .spm | Closed | Not planned |
| KeyShot | .bip | Closed | Not planned |
| Marmoset | .tbscene | Closed | Not planned |

### Web, AR/VR and Gaussian splats

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| Gaussian splats in PLY | .ply | Open | Next |
| SPZ | .spz | Open | Next |
| glTF Gaussian splats (KHR_gaussian_splatting) | .gltf .glb | Open | Next |
| Draco-compressed glTF | .drc, in glTF | Open | Next |
| meshopt-compressed glTF | in glTF | Open | Next |
| KTX2 / Basis textures | .ktx2 | Open | Next |
| SOG / Streamed SOG | .sog | Open | Later |
| SPLAT / KSPLAT | .splat .ksplat | Open | Later |
| LCC2 | .lcc | Closed | Later |
| Apple Reality | .reality | Closed | Not planned |
| Sceneform | .sfb | Closed, discontinued | Not planned |

### GIS, 3D city and terrain

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| CityJSON | .json .city.json .jsonl | Open | Opens |
| CityGML 1.0 / 2.0 | .gml .xml | Open | Opens |
| CityGML 3.0, IndoorGML, IMGeo | .gml | Open | Later |
| GeoJSON | .geojson .json | Open | Opens |
| Shapefile | .shp .dbf .shx | Documented | Opens |
| ASCII grid (terrain) | .asc | Open | Opens |
| Cesium 3D Tiles 1.0 / 1.1 | tileset.json, .b3dm .i3dm .pnts .cmpt .glb | Open | Next |
| quantized-mesh terrain | .terrain | Open | Next |
| GeoTIFF / COG (elevation) | .tif .tiff | Open | Next |
| Esri I3S / SLPK | .slpk | Open | Later |
| OSGB | .osgb | Documented in source only | Later |
| S3M | .s3mb | Open | Later |
| DTED | .dt0 .dt1 .dt2 | Open | Later |
| GeoPackage | .gpkg | Open | Later |
| FlatGeobuf | .fgb | Open | Later |
| FlatCityBuf | .fcb | Open | Later |
| KML / KMZ with COLLADA | .kml .kmz | Open | Later |
| Esri FileGDB multipatch | .gdb | Closed | Later |

### Point clouds, surveying and scanning

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| LAS / LAZ | .las .laz | Open | Opens |
| E57 | .e57 | Open | Opens |
| PTS | .pts | Open | Opens |
| PTX | .ptx | Open | Opens |
| PCD | .pcd | Open | Opens |
| ASCII XYZ | .xyz .txt .csv | Open | Opens |
| PLY (meshes and point clouds) | .ply | Open | Opens |
| COPC | .copc.laz | Open | Next |
| LAS 1.4 waveform | .las .wdp | Open | Later |
| EPT | ept.json and tiles | Open | Later |
| Potree 1 / 2 | cloud.js, metadata.json | Open | Later |
| Optech CSD | .csd | Documented | Later |
| TerraSolid | .fbi .bin | Documented | Later |
| Leica LGS / LGSx | .lgs .lgsx | Closed | Via export: E57 |
| ReCap | .rcp .rcs | Closed | Via export: E57 |
| FARO | .fls .fws .lsproj | Closed | Via export: E57 |
| RIEGL | .rxp .rdbx | Closed | Via export: LAS |
| TZF scans | .tzf | Closed | Via export: E57 |
| Z+F | .zfs | Closed | Via export: E57 |
| Topcon | .cl3 | Closed | Via export: E57 |
| Pointools | .pod | Closed | Via export: E57 |
| NavVis | own | Closed | Via export: E57 |
| Matterport | own | Closed | Via export: E57 or OBJ |
| Photogrammetry projects (Metashape, Pix4D, RealityCapture) | .psx .p4d .rcproj | Closed | Via export: OBJ, PLY or LAS |

### 3D printing

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| STL | .stl | Open | Opens |
| 3MF core | .3mf | Open | Opens |
| AMF | .amf | Open | Opens |
| OFF | .off | Open | Opens |
| 3MF Production and Materials extensions | .3mf | Open | Next |
| 3MF Beam Lattice and Slice extensions | .3mf | Open | Next |
| 3MF Volumetric, Displacement, Boolean, Secure extensions | .3mf | Open | Later |
| Bambu / Orca project | .gcode.3mf .3mf | Partly documented | Next |
| PrusaSlicer project | .3mf | Partly documented | Next |
| G-code (FDM) | .gcode | Open | Next |
| Prusa binary G-code | .bgcode | Open | Next |
| UltiMaker UFP | .ufp | Closed | Later |
| CLI (layer vectors) | .cli | Open | Later |
| Resin / MSLA (50+ formats) | .ctb .goo .sl1 .pwmo and others | Mixed | Not planned |
| SLC | .slc | Closed | Via export: STL |
| Materialise Magics | .mgx | Closed | Via export: STL |
| Simplify3D | .factory | Closed | Via export: STL |

### Dental

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| Scan exports (iTero, Medit, TRIOS) | .stl .ply .obj | Open | Opens |
| 3Shape DCM | .dcm | Closed | Via export: STL or PLY |
| exocad and Dentsply Sirona projects | .dentalproject .dxd .cdt | Closed | Via export: STL |

### Medical

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| DICOM with embedded STL or OBJ | .dcm | Open | Next |
| DICOM CT / MRI volumes | .dcm | Open | Not planned |
| NIfTI | .nii .nii.gz | Open | Not planned |
| NRRD, MetaImage, Analyze, MINC | .nrrd .mha .hdr .mnc | Open | Not planned |
| 3D Slicer scene | .mrb | Open | Not planned |
| Materialise Mimics | .mcs | Closed | Not planned |

### Heritage

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| Smithsonian Voyager SVX | .svx.json | Open | Next |
| IIIF Presentation 4.0 scene | .json | Open (draft) | Later |
| Artec, Creaform, Shining3D projects | .sproj and others | Closed | Via export: OBJ or PLY |

### Finite element analysis

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| FEM input deck | .inp | Documented text | Next |
| FEM bulk data | .bdf .nas | Documented text | Next |
| Finite element mesh | .msh .geo | Open | Next |
| FEM results | .op2 .f06 | Documented | Later |
| FEM model and results | .cdb .rst .rth | Partly documented | Later |
| FEM results database | .odb | Closed | Via export: VTU |
| FEM database, closed | .cdb | Closed | Via export: VTU |
| Explicit FEM model and results | .k, d3plot | Documented | Later |
| FEM results, open text | .frd | Open | Later |
| Universal file | .unv .uff | Open | Later |
| FEM neutral file | .neu | Documented | Later |
| FEM model with phases | .dat .dpf .fdb | Closed | Via export: VTU |
| Geotechnical model | .p2dx .p3dx | Closed | Via export: VTU |
| Zone and mesh files | .f3grid .mdpa .dato | Documented | Later |
| MED | .med .rmed | Open | Later |

### CFD and scientific visualisation

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| VTK legacy and XML, PVD | .vtk .vtu .vtp .vts .vtr .vti .pvtu .vtm .pvd | Open | Next |
| Exodus II | .exo .e | Open | Later |
| CGNS | .cgns | Open | Later |
| XDMF | .xdmf .h5 | Open | Later |
| CFD case folder | polyMesh and time folders | Open | Later |
| CFD mesh and case | .msh .cas .dat | Partly documented | Later |
| CFD simulation file | .sim .ccm | Closed | Via export: VTU |
| Plot data | .dat .plt | Documented | Later |
| Compressed plot data | .szplt | Closed | Via export: VTU |
| Case and geometry files | .case .geo | Documented | Later |
| CFD meshes | .su2 .ugrid .h5m | Open | Later |
| Multiphysics mesh and model | .mphtxt .mph | Text documented, model closed | Later |
| Silo / ADIOS2 | .silo .bp | Open | Later |

### Geology, mining, oil and gas, and the Dutch subsurface

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| GEF (soundings, boreholes) | .gef | Open | Next |
| BRO XML (CPT, boreholes) | .xml | Open | Next |
| GeoTOP / REGIS II (subsurface voxels) | NetCDF, CSV | Open data | Later |
| AGS4 / DIGGS | .ags .xml | Open | Later |
| SEG-Y (seismic) | .sgy .segy | Open | Later |
| RESQML | .epc .h5 | Open | Later |
| OMF | .omf | Open | Later |
| GOCAD ASCII | .ts .vs .pl .sg .vo | Documented | Later |
| ZMAP+ | .zmap | Documented | Later |
| Well logs (LAS log, DLIS, WITSML) | .las .dlis .xml | Open | Not planned |
| Surpac | .str | Documented text | Via export: OMF |
| Datamine | .dm | Closed | Via export: OMF |
| Vulcan | .00t | Closed | Via export: OMF |
| Leapfrog | .lfm | Closed | Via export: OMF |
| Petrel | .pet | Closed | Via export: RESQML |

### Earth and space sciences

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| NetCDF | .nc | Open | Later |
| HDF5 | .h5 | Open | Later |
| GRIB | .grib2 | Open | Not planned |
| FITS | .fits | Open | Not planned |
| Zarr | .zarr | Open | Not planned |

### Molecules and crystals

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| PDB / PDBx-mmCIF | .pdb .cif .bcif | Open | Not planned |
| Molecule and crystal files (CIF, MOL/SDF, MOL2, XYZ, CML, cube, POSCAR, GRO, MRC) | various | Documented | Not planned |

### Robotics

| Format | Extensions | Open or closed | Status |
|--------|------------|----------------|--------|
| URDF | .urdf .xacro | Open | Next |
| SDFormat | .sdf .world | Open | Later |
| MJCF | .xml | Open | Later |
| Robot programs (RAPID, KRL) | .mod .src | Closed | Not planned |

The list comes from a study of 3D formats made in November 2026; not every fact in it has been verified. Is your format missing, or should one move up? Ask for it in the [issues of the source repository](https://github.com/OpenAEC-Foundation/open-bim-suite/issues).

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
