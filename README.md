# build-glog-for-android
Build shared libraries of glog and gflags for android with ndk.

## How To
Export your android ndk root, pointing to the location of your ndk, could be something like below.
```
export ANDROID_NDK_ROOT=/home/<username>/Android/Sdk/ndk/<ndk_version>/
```

Clone glog and gflags into this repo.
```
git clone https://github.com/google/glog/
cd glog
git checkout  v0.4.0
cd ..

git clone https://github.com/gflags/gflags
cd gflags
git checkout v2.2.2
cd ..

## 设置NDK_ROOT, 设置SDK路径
bash build-glog.sh
```

If you want static libraries instead of shared libraries, set: `DBUILD_SHARED_LIBS=OFF` and `-DANDROID_STL="c++_static"` instead of `-DANDROID_STL="c++_shared"` in both scripts.
