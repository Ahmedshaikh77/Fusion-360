# Fusion 360 Design Portfolio

A collection of Autodesk Fusion CAD files covering numbered design studies, named mechanisms, and robot designs. The repository provides the original models for inspection, with a catalog that makes it easier to find a design and understand how its archive is packaged.

**32 CAD files · 23 basic designs · 7 advanced designs · 2 robot files**

## Start with these models

| Model | What to explore |
| --- | --- |
| [Robot Assemble](Robot/Robot%20Assemble.f3z) | A linked robot assembly archive. Its metadata identifies one root design and eight referenced design documents, including a base, links, and gripper-related designs. |
| [ArmBot](Robot/ArmBot%20v1.f3d) | A separate Fusion document in the robot collection. It is not listed as a dependency of the Robot Assemble archive. |
| [Geneva Wheel Mechanism](Advance%20Desing/Geneva%20Wheel%20Mechanism%20v1.f3d) | A mechanism study to explore in Fusion, including its geometry and any available joints. |
| [Engine, Piston & Crank Shaft](Advance%20Desing/Engine%20_%20Piston%20%26%20Crank%20Shaft%20v1.f3d) | The piston-and-crankshaft design from the mechanism collection. |
| [Cardan Joint](Advance%20Desing/Cardan%20Joint%20v1.f3d) | A joint design to review alongside [Ball Joint](Advance%20Desing/Ball%20Joint%20v0.f3d) and [Angular Transmitter Mechanism](Advance%20Desing/Angular%20Transmitter%20Mechanism%20v0.f3d). |

For every file, including the numbered studies, see the [CAD catalog and usage guide](docs/CAD_GUIDE.md).

## Quick start

You need access to Autodesk Fusion to inspect and edit the native models. The repository does not include the application or establish eligibility for an Autodesk license.

1. Download this repository, or choose a model from the catalog and download its original file from GitHub. Do not save the GitHub HTML page as a CAD file.
2. Keep the downloaded original unchanged. Make a working copy and use a separate Fusion project or review folder for your exploration.
3. Import the `.f3d` file, or upload the complete `.f3z` archive into Fusion. For **Robot Assemble**, keep the `.f3z` intact so its linked documents can be handled together.
4. Open the imported design and inspect its units, model tree, and any warnings before editing. For the robot bundle, open the root design named **Robot Assemble**.

The [usage guide](docs/CAD_GUIDE.md#open-and-explore-without-changing-the-originals) explains the archive types, duplicate names in the robot bundle, and what to check before experimenting.

## Repository map

| Folder | Files | Contents |
| --- | ---: | --- |
| [Basic Designs](Basic%20Designs/) | 23 `.f3d` | Design 1 through Design 23. The filenames do not specify individual part functions. |
| [Advance Desing](Advance%20Desing/) | 7 `.f3d` | Five named mechanisms or joints, plus Advance Design 1 and 2. The original folder spelling is retained. |
| [Robot](Robot/) | 1 `.f3d`, 1 `.f3z` | ArmBot and the linked Robot Assemble bundle. |
| [docs](docs/CAD_GUIDE.md) | Documentation | Full file catalog, archive contents, and review workflow. |

## What this portfolio provides

- Original Fusion files for examining CAD structure and mechanical design work.
- Numbered design studies, named mechanisms, and robot-related designs to discuss in a technical review.
- A linked assembly example whose packaged dependencies can be traced through the archive metadata.

This is a **CAD collection**, not a verified manufacturing release or a robot-control software package. No separate drawings, bill of materials, fabrication instructions, simulation reports, or physical test results are included. Dimensions, materials, constraints, motion behavior, and manufacturing suitability must be checked in the models; no performance claims are made here.

Archive contents and integrity were inspected for this documentation. The models have **not been opened or tested in Fusion as part of that review**. See [inspection scope](docs/CAD_GUIDE.md#inspection-scope) for the distinction.

## Feedback and contributions

For a question or proposed improvement, [open an issue](https://github.com/Ahmedshaikh77/Fusion-360/issues) with the exact model path, your Fusion version, a screenshot if useful, and the steps needed to reproduce the issue. Discuss model changes before replacing an archive, and keep the original files available for comparison.

Documentation corrections are welcome. Do not infer missing specifications from filenames or label an untested design as manufacturing-ready.

## License

These designs are provided for educational and reference purposes.

---

**Author**: Ahmed Shaikh  
**Repository**: [Fusion-360](https://github.com/Ahmedshaikh77/Fusion-360)
