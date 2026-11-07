# PixelOS

## Getting Started

To get started with the PixelOS source code, you'll need to be
familiar with [Git and Repo](https://source.android.com/setup/build/downloading).

To initialize your local repository, run:

```bash
repo init -u https://github.com/aobuta-prjkt/pixelos_manifest -b seventeen --git-lfs --depth=1
```

Then, sync the repository:

```bash
repo sync
```

## Building the System

Initialize the ROM build environment by sourcing the envsetup.sh script:

```bash
source build/envsetup.sh
```

After cloning the device-specific sources, use breakfast to configure the build for your device:

```bash
breakfast devicecodename
```

Start the compilation:

```bash
m pixelos
```

## Extras
To add maintaner name, add this in product / system prop:
```bash
ro.custom.maintainer=Your Name
```
Enable Perf anim override for MTK device:
```
PERF_ANIM_OVERRIDE := true
```

## Submitting Patches
Patches are always welcome! Feel free to submit your patches via [PixelOS Gerrit](https://review.pixelos.net/).
