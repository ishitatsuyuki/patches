# DRM hrtimer patches

This folder contains Linux kernel patches for improving DRM fence wait timeout accuracy.
This helps use cases where `vkWaitForFences()` is also used for pacing the submission loop.
