# FERP Script Bundles

This repository is a catalog of **FERP script bundles**.
Each bundle is distributed as a single `.ferp` file that can be downloaded and installed directly into FERP.

Individual bundles are self-contained and documented independently. This repository exists to organize, version, and distribute them in a consistent way.

---

## Repository structure

```
  ferp.<bundle_name>/
    <bundle_name>.ferp
    readme.md
  ...
```

### Conventions

* **One directory = one bundle**
* Each bundle directory contains:

  * A single **`.ferp` file** (the installable bundle)
  * A **`readme.md`** describing that specific script/bundle
* Bundle directories are prefixed with `ferp.` for clarity and namespace consistency

---

## What is a `.ferp` file?

A `.ferp` file is a **FERP bundle package**. It is the unit that users install into FERP.

A bundle includes:

* An executable scripts
* Metadata (name, description, version, entrypoints, readme)
* Configuration defaults
* Assets required at runtime

From the user’s perspective, the `.ferp` file is the only required artifact.

---

## Installing a bundle in FERP

1. Navigate to the bundle directory you want (for example: `ferp.hello_world/`)
2. Download the `.ferp` file
3. In FERP:

   * Open the **Command Palette** and select **Install Script Bundle** workflow
   * Enter the path to the downloaded `.ferp` file and select "Ok"
4. Once installed, the script will appear in FERP’s script list according to its bundle metadata

Refer to the **bundle’s own `readme.md`** for:

* What the script does
* Inputs / prompts
* Runtime requirements
* Expected behavior and outputs

---

## Bundle documentation

Each bundle directory contains its own `readme.md`.

Those READMEs are the **source of truth** for:

* Script purpose and scope
* Usage notes
* Limitations or warnings
* Any special configuration or environment requirements

This top-level README intentionally does **not** duplicate that information.

---

## Versioning

* Bundles are versioned internally (inside the `.ferp` file)
* The directory name does not imply version
* Updates to a bundle are published by replacing the `.ferp` file with a newer version

If you are distributing this repo as a Git submodule or download source, users should always rely on the bundle metadata—not Git history—for version identification.

---

## Safety and responsibility

FERP bundles may perform file system operations such as:

* Renaming or moving files
* Reading or transforming documents
* Writing output files

Users should:

* Review the bundle README before installing
* Test on non-production data when possible
* Only install bundles from trusted sources

---

## License

See the `LICENSE` file in zappbrandigan/ferp-scripts for script-level licensing information.
