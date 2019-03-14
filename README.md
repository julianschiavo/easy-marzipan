# easy-marzipan
Resources and workarounds to improve and make it easier to use Marzipan at the current stage.

## [Cheatsheet](cheatsheet.md)
A list of unavailable/missing frameworks, methods, and selectors. Allows you to quickly check what's not available on Marzipan without having to go through the build cycle repeatedly.

## [Workarounds](workarounds.swift)
Compilation of patches to add missing selectors such as `-[NSFont isSystemFont]`, which is called when you use Dynamic Type. Import this file into your project to fix issues that are caused by UIKit internally.
