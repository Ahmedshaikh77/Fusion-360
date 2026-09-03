# CAD catalog and usage guide

[Back to the portfolio README](../README.md)

This catalog covers all **32 CAD files** in the repository. Names and version suffixes below reproduce the actual filenames. A suffix such as `v0`, `v1`, or `v2` is a file label, not a statement about testing, maturity, or compatibility with a particular Fusion release.

## Basic designs

The `Basic Designs/` folder contains 23 numbered `.f3d` files. Their individual functions are not documented in the filenames, so this guide does not assign guessed part names or manufacturing uses.

| Design | Original file |
| --- | --- |
| 1 | [Design 1 v1.f3d](../Basic%20Designs/Design%201%20v1.f3d) |
| 2 | [Design 2 v1.f3d](../Basic%20Designs/Design%202%20v1.f3d) |
| 3 | [Design 3 v1.f3d](../Basic%20Designs/Design%203%20v1.f3d) |
| 4 | [Design 4 v1.f3d](../Basic%20Designs/Design%204%20v1.f3d) |
| 5 | [Design 5 v1.f3d](../Basic%20Designs/Design%205%20v1.f3d) |
| 6 | [Design 6 v1.f3d](../Basic%20Designs/Design%206%20v1.f3d) |
| 7 | [Design 7 v2.f3d](../Basic%20Designs/Design%207%20v2.f3d) |
| 8 | [Design 8 v1.f3d](../Basic%20Designs/Design%208%20v1.f3d) |
| 9 | [Design 9 v1.f3d](../Basic%20Designs/Design%209%20v1.f3d) |
| 10 | [Design 10 v1.f3d](../Basic%20Designs/Design%2010%20v1.f3d) |
| 11 | [Design 11 v1.f3d](../Basic%20Designs/Design%2011%20v1.f3d) |
| 12 | [Design 12 v1.f3d](../Basic%20Designs/Design%2012%20v1.f3d) |
| 13 | [Design 13 v1.f3d](../Basic%20Designs/Design%2013%20v1.f3d) |
| 14 | [Design 14 v1.f3d](../Basic%20Designs/Design%2014%20v1.f3d) |
| 15 | [Design 15 v1.f3d](../Basic%20Designs/Design%2015%20v1.f3d) |
| 16 | [Design 16 v1.f3d](../Basic%20Designs/Design%2016%20v1.f3d) |
| 17 | [Design 17 v1.f3d](../Basic%20Designs/Design%2017%20v1.f3d) |
| 18 | [Design 18 v1.f3d](../Basic%20Designs/Design%2018%20v1.f3d) |
| 19 | [Design 19 v1.f3d](../Basic%20Designs/Design%2019%20v1.f3d) |
| 20 | [Design 20 v1.f3d](../Basic%20Designs/Design%2020%20v1.f3d) |
| 21 | [Design 21 v1.f3d](../Basic%20Designs/Design%2021%20v1.f3d) |
| 22 | [Design 22 v1.f3d](../Basic%20Designs/Design%2022%20v1.f3d) |
| 23 | [Design 23 v0.f3d](../Basic%20Designs/Design%2023%20v0.f3d) |

## Advanced designs

The folder is spelled **`Advance Desing/`** in the repository. These are seven separate `.f3d` files; links preserve that spelling and the original filenames.

| Model label | Original file |
| --- | --- |
| Advance Design 1 | [Advance Design 1 v1.f3d](../Advance%20Desing/Advance%20Design%201%20v1.f3d) |
| Advance Design 2 | [Advance Design 2 v1.f3d](../Advance%20Desing/Advance%20Design%202%20v1.f3d) |
| Angular Transmitter Mechanism | [Angular Transmitter Mechanism v0.f3d](../Advance%20Desing/Angular%20Transmitter%20Mechanism%20v0.f3d) |
| Ball Joint | [Ball Joint v0.f3d](../Advance%20Desing/Ball%20Joint%20v0.f3d) |
| Cardan Joint | [Cardan Joint v1.f3d](../Advance%20Desing/Cardan%20Joint%20v1.f3d) |
| Engine, Piston & Crank Shaft | [Engine _ Piston & Crank Shaft v1.f3d](../Advance%20Desing/Engine%20_%20Piston%20%26%20Crank%20Shaft%20v1.f3d) |
| Geneva Wheel Mechanism | [Geneva Wheel Mechanism v1.f3d](../Advance%20Desing/Geneva%20Wheel%20Mechanism%20v1.f3d) |

These names identify the intended subjects. They do not establish joint limits, drive relationships, loads, tolerances, or simulation results.

## Robot designs

| Original file | Packaging |
| --- | --- |
| [ArmBot v1.f3d](../Robot/ArmBot%20v1.f3d) | One Fusion document archive. Kept separately from Robot Assemble; no relationship between the two models is asserted here. |
| [Robot Assemble.f3z](../Robot/Robot%20Assemble.f3z) | A bundle containing nine `.f3d` documents, `Manifest.json`, and `DesignDescription.json`. |

### Inside Robot Assemble

The archive's `Manifest.json` identifies the root file. `DesignDescription.json` names that design **Robot Assemble** and records eight `XREF` dependencies. All nine listed `.f3d` entries are present in the bundle.

| Display name in metadata | Documents | Recorded versions | Role |
| --- | ---: | --- | --- |
| Robot Assemble | 1 | 1 | Root design; references the other eight documents. |
| Base 6dof | 1 | 1 | Referenced design. The name is not evidence of an independently verified degree-of-freedom count. |
| Link 1 | 1 | 1 | Referenced design. |
| Link 2 | 2 | 1 and 1 | Two distinct design entries with different internal identifiers. |
| Link 3 | 1 | 1 | Referenced design. |
| Gripper | 2 | 1 and 3 | Two distinct design entries, not a reason to discard either file. |
| Gripper Support | 1 | 1 | Referenced design. |

The internal files use identifier-based filenames. Do not extract the bundle, rename the files to their display names, and overwrite similarly named entries: **Link 2** and **Gripper** each occur twice. Import the original `.f3z` together instead.

## File formats in this repository

| Format | What it contains here | How to handle it |
| --- | --- | --- |
| `.f3d` | A native Fusion document archive containing manifests, design data, and an embedded preview. There are 31 at repository level. | Work from a duplicate. Import into Fusion to inspect the design, rather than editing the archive's internal files. |
| `.f3z` | The Robot Assemble distribution bundle, including the root document, referenced documents, and the dependency description. | Upload the complete bundle to a separate Fusion project or review folder and open its root design. |

If you download the whole repository as a GitHub `.zip`, unpack that outer ZIP to reach the model files. Leave the `.f3d` and `.f3z` model archives unchanged. A generic ZIP utility is not a substitute for Fusion import; some model entries use compression that older ZIP tools may not support.

## Open and explore without changing the originals

1. **Keep a baseline.** Retain the downloaded archive with its original filename. Make a separate working copy before importing or experimenting.
2. **Use an isolated destination.** In Autodesk Fusion, choose a separate project or review folder that will not overwrite an existing design. Menu labels and import behavior can vary with the installed release.
3. **Import the correct level.** Use the `.f3d` for an individual design. For Robot Assemble, upload the complete `.f3z`, not just one of its embedded documents.
4. **Confirm the import.** Open the expected design. For the bundle, select **Robot Assemble** and check that referenced designs are resolved. Do not assume that equal display names mean duplicate content.
5. **Inspect before editing.** Check document units, component/body organization, any available design history or sketches, and warnings. If joints are present, review their constraints and limits before testing motion.
6. **Save experiments separately.** Use a distinct project/design name for your work. If you duplicate an imported assembly, confirm whether it still references the original imported components before editing those components. A renamed parent alone should not be treated as an independent copy of every dependency.
7. **Record what you observe.** Keep screenshots and notes about the specific model, software version, warning messages, and any changes. Do not replace the original repository archive with an experimental export.

The expected first result is a loaded design that you can inspect. It is not a guarantee of fully constrained sketches, working motion simulation, or fabrication readiness.

## Before proposing a model update

- Identify the exact original file and explain the problem or intended improvement.
- Include screenshots and a reproducible review procedure.
- Keep changed files separate until the maintainer agrees on naming and scope.
- For linked assemblies, retain the dependency structure and check for unresolved references after import.
- Distinguish visual observations from measured, simulated, or physically tested results.
- Preserve existing attribution and the repository's usage statement.

For an import failure, report the original path, Fusion version, exact error, and whether it affects an individual `.f3d` or the complete `.f3z`. Avoid renaming extensions or deleting dependencies as a workaround.

## Inspection scope

This guide was checked against the repository's tracked filenames and read-only archive inspection:

- All 32 repository-level CAD archives were enumerated and their member integrity checks passed.
- Each of the 31 repository-level `.f3d` archives contains manifests, design data, and `FusionAssetName[Active]/Previews/small.png`.
- Robot Assemble contains the nine `.f3d` documents listed by its JSON metadata. Integrity checks also passed for those nested archives.
- The root design and its eight references were matched to the packaged files. Repeated display names were retained as separate entries.

Archive integrity only shows that the packaged data can be read; it does **not** validate geometry, Fusion application compatibility, constraints, kinematics, materials, strength, or manufacturability. No original CAD file was modified, re-exported, or opened in Fusion during this documentation review. The repository does not include separate drawings, BOMs, manufacturing instructions, simulation reports, or physical test records.
