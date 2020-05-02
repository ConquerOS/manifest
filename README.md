![ConquerOS](https://raw.githubusercontent.com/ConquerCAF/manifest/ten/logo.png)

# ConquerOS 3.X
ConquerOS is a simple CAF Based Custom ROM with additional features and UI/UX improvement to give user good experience when using it.

## Compilation of ConquerOS

### 1. Requirements
Before start to compiling ConquerOS for your own device, you need to complete some requirements as explained bellow:
```
- AMD64{64bit} based Linux system.
- 250GiB Free disk space(Recommended to use SSD).
- Quad-core processor.
- 16GiB RAM(Swap also can help).
- Fast and helpful internet connection.
```

### 2. Preparation
We have completed the requirements. Now, let's start to prepare compilation environtment. Cause all people isn't use same Linux distribution. So, let's make more simple with @akhilnarang 's script.
```
git clone https://github.com/akhilnarang/scripts
cd scripts
. setup/*sh
```

### 3. Downloading ConquerOS Source
Now, let's download ConquerOS Source

- First, make directory for ConquerOS Source, and then enter to the directory.
```
mkdir -p ~/conquer
cd /conquer
```

- Second, initialize ConquerOS Source manifest in the directory
```
If you want to download full ConquerOS Source, type:
repo init -u https://github.com/ConquerOS/manifest.git -b ten

But, if you want to do shallow download, type:
repo init --depth=1 -u https://github.com/ConquerOS/manifest.git -b ten

NOTES: Shallow download will not include full commits history.
```

- Third, start downloading the ConquerOS Source.
```
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### 4. Download device sources
We can't compile ConquerOS without device source code. So, you need to clone device tree, Kernel source, vendor tree, and maybe your device use some common trees.

### 5. Start compilation
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
mka carthage -jX
```

## Notes
- Whenever you see "-jX" the, you need to change "X" with number of your complier machine's thread number.
- For maintainership infomation, please cask on our [Telegram group](http://t.me/ConquerOSChat).
![ConquerOS 3.X Based on Android 10](https://raw.githubusercontent.com/ConquerCAF/manifest/ten/version.png)
