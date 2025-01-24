#

### Create a directory for the source files & Go into created directory
```
mkdir workspace
```
```
cd workspace
```
### Initializing Repo
```
repo init -u https://github.com/Tequila-Extended/platform_manifest.git -b uno --git-lfs
```

### Now sync sources
```
repo sync -c --no-clone-bundle --optimized-fetch --prune --force-sync -j$(nproc --all)
```

### Now run
```
. build/envsetup.sh
```
```
mka bacon -j$(nproc --all)
```
