# Experimental WAIPIO kernel 6.6 configuration

**Native25 and Package-23b use kernel 5.10.246.** This directory contains separate
6.6 build configuration for experimental builds.

A device using this configuration sets `TARGET_USES_KERNEL_6_6 := true` before
including `BoardConfigCommon.mk`. It needs matching WAIPIO/Ferrari changes in
`kernel/oneplus/sm8750`, `sm8750-modules` and `sm8750-devicetrees`.
The build uses Android Make/Kbuild integration.

Ferrari's 6.6 configuration selects WAIPIO v1/v2 base device trees and the combined
board/audio/display/camera overlay. Keep those overlays and module lists matched
to the 6.6 source. The combined overlay replaces the older split techpack overlays.

Full Android kernel/module build and device-boot testing for this 6.6 configuration
remain incomplete. Use the release's [documented 5.10 source](https://github.com/wjdob/lineageos-realmegt2pro/blob/lineage-24.0/SOURCES.md)
when inspecting or reproducing Native25.
