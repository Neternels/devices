## Build Information
```
Kernel: NetErnels Kernel
Type: Stable
Device: Redmi Note 10
Compiler: Eva GCC 12.0.0
Branch: LA.UM.9.1
Build Number: v6-NYSP
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
