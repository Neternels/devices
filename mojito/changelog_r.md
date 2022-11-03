## Build Information
```
Kernel: NetErnels Kernel
Type: Bleeding Edge
Device: Redmi Note 10
Compiler: Eva GCC 12.2.1
Branch: staging
Build Number: r16b13
```
## Changelog
**-r16b14**

* Drop MGLRU as its too aggressive.
* Drop SLMK tunables.
* Dynamically tune minfree and timeout values of SLMK.
* QoL patches to net and qcacld to improve wlan perf.
* Remove rmnet drivers for wlan perf.
* Drop multiple kswapd threads per node as it does not provide any significant benefits whilst having 4% cpu usage per boot.
* Increase throttle temp for fast charging to 42.

**-r16b13**

* Enable LZ4 for F2FS Compression.
* Kill SDCardFS when flashed in an inline build (PixelOS Only for now).
* Enable Legacy QTI MSM RNG support.
* Grab MGLRU from android-4.14-stable gerrit.
* Add Simple_LMK hooks to MGLRU.
* Misc CFQ improvements.
* Linked with LLD 16.0.0.
