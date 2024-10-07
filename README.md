# Reproducer for Safari/iOS 18 bug where getUserMedia video track getSettings() returns stale value for torch constraint

This repository illustrates a bug in Safari on iOS 18 where getting video track settings appears to return stale
values for the `torch` constraint (flashlight on smartphones).

The value returned for the torch constraint appears to be "stale" in the sense that it does not reflect the current
value. After setting the `torch` constraint to `true`, getSettings() returns it as `false`.
Setting it back to `false` causes getSettings() to return it as `true`.
