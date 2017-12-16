# download source

repo init -u git://github.com/LineageOS/android.git -b cm-14.1

mkdir .repo/local_manifests

copy ${PATH_TO}/zerofltechn.xml .repo/local_manifests/

repo sync

# build

. build/envsetup.sh

breakfast zerofltechn

make bacon -j8
