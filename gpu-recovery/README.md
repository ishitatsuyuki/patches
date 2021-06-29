# GPU recovery patches

This folder contains patches to enable better recovery behaviors in case of GPU timeout. Currently, two set of patches are available:

1. Kernel patches for AMDGPU soft-recovery  
The upstream kernel currently does not deliver an error to the application that triggered a timeout when soft-recovery is used. This patch fixes the issue and makes it more likely that the offending application terminates.
2. Mesa patch for AMDGPU soft-recovery  
Currently the radeonsi driver notifies the application of a GPU reset in the case of soft recovery even when the application is unaffected and does not need to recreate anything. This patch suppresses such irrelevant notifications. It should be used in combination with the kernel patches so that a context reset still occurs when the application is actually the offender.
