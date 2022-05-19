![](LESSAOSP.png)

# HOW TO BUILD LESSAOSP ROM?

create a directory called as **lessaosp**

## Initialize local repository inside lessaosp folder
```## Initialize local repository
repo init -u https://github.com/LessAospOS/manifest -b 12.1
```

## For users below 250GB Storage Limit use below shallow clone
```## for below 250GB users use below shallow clone 
repo init -u https://github.com/LessAospOS/manifest -b 12.1 --depth=1
```
## Sync
```## Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
# Build Process
```## Set up environment
. build/envsetup.sh
```

## Choose a target
```## Choose a target
lunch aosp_$device-userdebug
```
## Build the code
```## Build the code
make bacon -jX
```
# Credits
* [PixelExperience](https://github.com/PixelExperience)
* [Project-Awaken](https://github.com/Project-Awaken)
* [Lineage](https://github.com/LineageOS)
