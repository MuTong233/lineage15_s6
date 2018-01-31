# download source
# Use Tsinghua Mirror to acclerate (China Users)
# UNTEST
```
repo init -u https://mirrors.tuna.tsinghua.edu.cn/lineageOS -b staging/lineage-15.1
mkdir .repo/local_manifests
copy ${PATH_TO}/zerofltechn.xml .repo/local_manifests/
repo sync
```
# build
```
. build/envsetup.sh
breakfast zerofltechn
make bacon -j8
```
