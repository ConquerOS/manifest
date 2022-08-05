![conquerOS](https://raw.githubusercontent.com/conquerOS/manifest/twelve/banner.png)

# conquerOS Sundew [![Download conquerOS](https://img.shields.io/sourceforge/dt/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)  [![Download conquerOS](https://img.shields.io/sourceforge/dm/conqueros.svg)](https://sourceforge.net/projects/conqueros/files/latest/download)
conquerOS is a simple CAF Based Custom ROM with additional features and UI/UX improvement to give user good experience when using it.

## Building conquerOS

### Requirements
Before start to compiling conquerOS for your own device, you need to complete some requirements as explained bellow:
- 16GB RAM (Swap can be helpful)
- Quadcore Processor
- 300GB Free Disk Space (Recommended to use SSD)
- Internet conncection

### Download conquerOS Source
Now, let's Download conquerOS Source

- First, make directory for conquerOS Source, and then enter to the directory.
```
 mkdir -p ~/conquer
 cd ~/conquer
```

- Second, initialize conquerOS Source manifest in the directory
```
 repo init -u https://github.com/ConquerOS/manifest.git -b twelve
```

- Just in case you just want save more space and data, you can use command below
```
 repo init --depth=1 -u https://github.com/ConquerOS/manifest.git -b twelve
```

- Third, start downloading the conquerOS Source.
```
 repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Start building
Now, let's start compilation

- Call building environtment setup script.
```
 source build/envsetup.sh
 lunch conquer_<device_codename>-userdebug
 make carthage -j$(nproc --all)
```

For more information, you can check our [Wiki](https://wiki.conquerOS.co)

## Follow us
- [Twitter](http://twitter.com/conquerOSROM)
- [Telegram News Channel](http://t.me/conquerOSNews)
- [Telegram Updates Channel](http://t.me/conquerOSUpdates)
- [Telegram Group](http://t.me/conquerOSChat)
