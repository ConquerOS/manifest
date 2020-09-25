![ConquerOS](https://raw.githubusercontent.com/ConquerOS/manifest/ten/logo.png)

# ConquerOS 4.X Raven Alpha [![Download ConquerOS](https://img.shields.io/sourceforge/dt/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)  [![Download ConquerOS](https://img.shields.io/sourceforge/dm/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)  
ConquerOS is a simple CAF Based Custom ROM with additional features and UI/UX improvement to give user good experience when using it.

```
ConquerOS 4 Raven is still on Aplha stage, which mean there no support for this version yet untill Stable release.
```

## Building ConquerOS

### 1. Download ConquerOS Source
```
$ repo init -u https://github.com/Conquer-Staging/manifest -b eleven
$ repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### 2. Start building
```
$ . build/envsetup.sh
$ lunch conquer_DEVICE-userdebug
```
