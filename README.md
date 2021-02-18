![ConquerOS](https://raw.githubusercontent.com/ConquerOS/manifest/ten/logo.png)

# ConquerOS 4.X Raven Beta [![Download ConquerOS](https://img.shields.io/sourceforge/dt/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)  [![Download ConquerOS](https://img.shields.io/sourceforge/dm/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)  
ConquerOS is a simple CAF Based Custom ROM with additional features and UI/UX improvement to give user good experience when using it.

## Building ConquerOS

### Requirements
Before start to compiling ConquerOS for your own device, you need to complete some requirements as explained bellow:
- 16GB RAM (Swap can be helpful)
- Quadcore Processor
- 300GB Free Disk Space (Recommended to use SSD)
- Internet conncection

### Download ConquerOS Source
Now, let's Download ConquerOS Source

- First, make directory for ConquerOS Source, and then enter to the directory.
```
mkdir -p ~/conquer
cd /conquer
```

- Second, initialize ConquerOS Source manifest in the directory
```
If you want to download full ConquerOS Source, type:
repo init -u git://github.com/ConquerOS/manifest.git -b eleven
```

- Just in case you just want save more space and data, you can use command below:
```
repo init --depth=1 -u git://github.com/ConquerOS/manifest.git -b eleven
```

- Third, start downloading the ConquerOS Source.
```
repo sync -c --no-clone-bundle --no-tags --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### Start building
Now, let's start compilation

- Call building environtment setup script.
```
. build/envsetup.sh
```

- Pick target device.
```
lunch conquer_DEVICE_NAME-userdebug
```

- Start the compilation.
```
make carthage -jX
```

## Follow us
- [Twitter](http://twitter.com/ConquerOSROM)
- [Telegram News Channel](http://t.me/ConquerOSNews)
- [Telegram Updates Channel](http://t.me/ConquerOSUpdates)
- [Telegram Group](http://t.me/ConquerOSChat)
