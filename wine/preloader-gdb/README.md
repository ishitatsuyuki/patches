# Improved debugging support for Wine preloader

The preloader currently prevents the debugger from resolving symbols in loaded shared libraries.
This patch fixes it and provides a better debugging experience with Wine.
