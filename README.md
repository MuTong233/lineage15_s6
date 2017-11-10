1. download source

repo init -u git://github.com/LineageOS/android.git -b cm-14.1
mkdir .repo/local_manifests
copy ${PATH_TO}/zerofltechn.xml .repo/local_manifests/
repo sync

2. apply patches

copy ${PATH_TO}/framework_av.patch frameworks/av/
cd frameworks/av/
git apply framework_av.patch
cd -

3. build

. build/envsetup.sh
breakfast zerofltechn
make bacon -j8
