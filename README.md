# ZMK Behavior Inverting Key Press Module

This is a module for a very simple behavior. It acts exactly like `&kp`, except if the key is already pressed it will invert the press. If you toggle `A` on and then press `&kp A`, you get a sequence like this:

```
&kt A pressed -> PRESS A
&kp A pressed -> PRESS A
&kp A released -> RELEASE A
```

The `&kp` will cancel the toggle. If you use `&ikp` instead, then you get a sequence like this:

```
&kt A pressed -> PRESS A
&ikp A pressed -> RELEASE A
&ikp A released -> PRESS A
```

The primary use for this is in gaming, where this allows you to bind multiple buttons to the same key and mash them fearlessly. My use case for this is WASD walking, letting me toggle `W` on and then press `&ikp W` when I want to stop for a moment.

## Usage

1. Follow the instructions on [modules](https://zmk.dev/docs/features/modules) to add this module to your build.
2. Include the definition of `&ikp` at the top of your keymap:

```dts
#include <behaviors/ikp.dtsi>
```

3. Use `&ikp` anywhere you desire in your keymap
