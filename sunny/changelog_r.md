## Build Information
```
Kernel: NetErnels Kernel
Type: Bleeding Edge
Device: Redmi Note 10
Compiler: Eva GCC 14.0.0
Branch: staging
Build Number: r17a7
```
## Changelog
**-r17a7**
* Add support for Android 14.
* Fixup kernel-level blocker for userspace irq balancer to not be utilized when init.is_sbalance=1.

**-r17a6**
* Implement screen state tracking for exposure adjustment which is used for DC Dim Schedule to fix black screen of deaths.
* Upstream KProfiles to `v6.0.0`.
* Drop perf-critical API as it is useless.
* Drop sched_migrate_to_cpumask_{start,end}() as it is also useless.
* Improve random memory access for EROFS.
* Misc improvements done to F2FS.
* Implement kernel-level IRQ Balancing which is known as SBalance.
* Implement a kernel-level blocker for userspace irq balancer.
* Add cmdline interface to check if SBalance is used.
* Do not utilize the blocker if init.is_sbalance=1 is implemented in cmdline.
* Add support for Sony DualSense and DualSense Edge controllers.
* Drop CAF's vmpressure based process reclaim.
* Enable Linux's Per-Process Reclaim to utilize it alongside CachedAppOptimizer.
* Build with EvaGCC 14.0.0.

**-r17a5**
* Transition to LMKD.
* Revert some harmful high-prio wq patches.
* Build kernel fully with GCC and GNU Binutils.
* Merge LA.UM.9.1.r1-12900-SMxxx0.0 in kernel.
* Update F2FS from f2fs-stable.
* Fix OOM crash when using "livin' by mandiri" banking application.

**-r17a4**
* Implement simple single tap attribute for modernized ST2W sensor.
* Add cmdline interface to check if st2w sensor is used.
* Restore legacy st2w behaviour.

**-r17a3**
* Re-expose SLMK tunables to userspace.
* Re-enable userspace CPU boosting.

**-r17a2**
* Add cmdline interface to check if dt2w sensor is used.
* Restore legacy dt2w behaviour.
* Guard double tap attribute handling(it breaks modernized dt2w if not adapted to this change).
* Stop building compressed Image as it's redundant.

**-r17a1**
* KProfiles 5.0.2.
* TP driver cleanup(kudos to fiqri).
* Minor DRM cleanup(kudos to fiqri).
* Implement simple double tap attribute for modernized dt2w sensor.
* Enable TouchGestures for double tap attribute to work.
* Fix touch suspend workqueue.
* Drop legacy double tap to wake handling.
* Simplify event key reporting.
* Rename gesture macros for sanity.
* Don't read gestures if TS has not suspended.
* Report SCHED_CAPACITY_SCALE to the problematic userspace for unity games.
* Add per-cpu threads for decompression in EROFS for better app launches and boot time.
* Set scheduler to use SCHED RR at high priority for lower latency.
* Drop TEO governor.
* Drop recent lpm-levels optimizations.
* Fully switch to WFI for cpuidle(should improve drains).
* Upgrade ZSTD to latest upstream v1.5.4.
* Fix HBM parameters to make HBM finally work.
* Restore brightness value when hbm is turned off.
* Implement exposure adjustment to have proper DC Dimming working.
* Adapt exposure adjustment values for sunny to have low flickering and minimal backlight intensity.

**-r16b15**
* Don't optimize wlan and audio drivers for size.
* Add support for /sys/touchpanel/double_tap node.
* Update in-kernel LZ4 to v1.9.4.
* Disable LZ4HC support.
* Increase rating of teo cpuidle governor to 50 so it supercedes qcom cpuidle governor.

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
