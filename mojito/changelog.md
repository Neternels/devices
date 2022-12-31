## Build Information
```
Kernel: NetErnels Kernel
Type: Stable
Device: Redmi Note 10
Compiler: Eva GCC 12.2.1
Branch: LA.UM.9.1
Build Number: v7-NYSP
```
## Changelog
**-v5**

* rebased over LA.UM.9.1.r1-11300-SMxxx0.0
* imported wlan drivers, audio drivers and rmnet off LA.UM.9.1.r1-11300-SMxxx0.0
* optimized for size with -Os and nuke debug information with -g0
* init touch driver earlier to not conflict with display notifiers
* sync latest kprofiles with lots of changes and features
* force set frequencies to max/min depending on mode set in kprofiles for performance governor
* add STREEBOG russian cryptographic algorithm
* cfq improvements
* nuked some logging in binder
* nuked some logging treewide
* reduce verbosity of vibrator logs
* force apps to use TCP_NODELAY to improve network latency
* calculate and use an optimized energy table for low power consumption
* calculate and use most efficient frequency table for high perf low power cost
* configure CIB according to set eff freqs
* configure idle minimum frequency of CIB for LP and HP clusters
* configure minimum frequency fallback of CIB for LP and HP clusters
* switch to 50hz tickrate
* rewire fingerprint driver for performance
* nuked IRQ affining for touch and fp
* improved the scheduler by picking a plethora of patches from RenderBroken
* nuked bfq and zen iosched
* reduce wake boost duration of devfreq_boost and cib
* nuke some qcacld logging
* switch to msm drm notifier for fp
* reduce time taken for fp to process and unlock by 1000ms
* force gpu idle timeout to 58ms
* implement rhel's low latency cmdline
* disable kpti hardening
* disable broken irq detection
* nuke lots of debugging
* enable freq-energy-model for {"sched/energy: checkout to android-4.14-stable"}
* pass quiet to cmdline for less verbose output during boot
* use 67us for cdsp
* compile out ipav3 wakelock code
* nuke pm qos changes in vidc
* use relr relocation packing
* backport and adapt binder from android-4.19-stable
* backport an important fix for put_page() from mainline
* backport TCP optimizations from mainline for reduced network latency and overall consistent network speed
* mainlined ZSTD
* use ZSTD for zswap as zstd proves to be better for zswap and other crypto operations

**-v6-NYSP**
* Rebased off LA.UM.9.1.r1-11400-SMxxx0.0
* Imported wlan drivers, audio drivers and rmnet off LA.UM.9.1.r1-11400-SMxxx0.0
* debloated Xiaomi changes 
* nuked some suntana ricing
* fix OTG issues
* upstream kernel/modules.c
* fix modules loading issues
* fix some unnecessary drains
* fix whatsapp web reconnecting issue
* backport AF_UNIX from mainline
* nuke some irrelevant logspam
* nuke irrelevant drivers
* fix vid recording in A12
* build most drivers as a module

**-v7-NYSP**
* Rebased off LA.UM.9.1.r1-11900-SMxxx0.0.
* Import wlan drivers from LA.UM.9.1.r1-11900-SMxxx0.0.
* Import audio drivers from LA.UM.9.1.r1-11900-SMxxx0.0.
* Import rmnet drivers from LA.UM.9.1.r1-11900-SMxxx0.0.
* Upstream F2FS from kernel/msm-4.14.
* Import ximi thermal changes.
* Some improvements done to schedutil.
* Tune CIB and devfreq_boost well with efficient frequency setup.
* Switch to 50hz tickrate.
* Drop lotta debugging and logging.
* Drop statfs and iostat for f2fs.
* Drop some unnecessary drivers from building.
* Vidc patches to improve video quality / video streaming.
* ZSTD optimizations by samsung.
* Drop DEBUGFS.
* CFQ patches for better I/O perf.
* Configure up/down ratelimit of schedutil for each cluster.
* Bring back full support for CAF ROMs.
* Enable LZO, LZO-RLE, LZ4, LZ4HC for f2fs compression.
* Backport exfat from mainline.
* Some DTS fixes for thermal.
* Backport an important network fix from mainline.
* LZ4 backports.
* EROFS backports.
* Parallel direct-writes backport (and enable the feature).
* Disable broken IRQ detection.
* Disable GCSE.
* Thermal patches (for step-wise).
* Drop MSM_THERMAL_SIMPLE.
* Switch to step_wise thermal governor.
* KGSL improvements by sultan.
* Some scheduler optimizations.
* Arter's KGSL patches.
* Backport an important mm patch to fix non atomic order 0 allocation failure from mainline.
* Debloat & Optimize the kernel (by dropping most irrelevant tracers and debugging drivers).
* Enable LZ4 compressed ramdisk (for those on roms that support it).
* Adapt boost events to latest KProfiles.
* Drop big core affines.
* Freq table and EM imported from gulch for consistency.
* Port over CRNG from LKS 4.14 to MSM-4.14.
* Drop Srandom over CRNG.
* Nuke extraneous FPC driver
* Implement IRQF_FORCE_RESUME correctly.
* Reduce memory usage of LZ4 to 16KB.
* Switch to LZ4 for pstore compression.
* Refactor the fingerprint driver for clarity.
* Build debugfs as of /sys/kernel/debug/tracing for ROMs with tracing and/or apps that require tracing.
* Stub out aw87xxx loggers for sanity.
* Kill qcacld wakelocks.
* Force warm reboots to preserve ramoops.
* Build debugfs as of /sys/kernel/debug/tracing for ROMs with tracing and/or apps that require tracing.
* Nuke irrelevant sched features which caused overhead (improved interactivity).
* EROFS fixes for random reboots.
* Improvements to power driver.
* Improvements to thermals (mi thermald should work better now).
* Improvements to touch driver (its cleaner now).
* Misc sched changes to improve latency.
* Rewire FPC driver for clarity (again).
* Enable LZ4 for F2FS Compression.
* Kill SDCardFS when flashed in an inline build (Supported ROMs only for now).
* Enable Legacy QTI MSM RNG support.
* Misc CFQ improvements.
* Increase throttle temp for fast charging to 42.
* Dynamically tune minfree and timeout values of SLMK.
* QoL patches to net and qcacld to improve wlan perf.
* Remove rmnet drivers for wlan perf.
* Don't optimize wlan and audio drivers for size.
* Add support for /sys/touchpanel/double_tap node.
* Update in-kernel LZ4 to v1.9.4.
* Disable LZ4HC support.
* Increase rating of teo cpuidle governor to 50 so it supercedes qcom cpuidle governor.
* Import OPLUS Memory Management Hacks.
* KProfiles 5.0.0.
* Built using GCC compiled from stable sources + LLVM from mainline.
