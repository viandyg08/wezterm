# CopyTo(destination)

Copy the selection to the specified clipboard buffer.

Possible values for destination are:

* `Clipboard` - copy the text to the system clipboard.
* `PrimarySelection` - Copy the test to the primary selection buffer (applicable to X11 and some Wayland systems only)
* `ClipboardAndPrimarySelection` - Copy to both the clipboard and the primary selection.

```lua
local wezterm = require 'wezterm';
return {
  keys = {
    {key="C", mods="CTRL", action=wezterm.action{CopyTo="ClipboardAndPrimarySelection"}},
  }
}
```

*Since: nightly builds only*

`PrimarySelection` is now also supported on Wayland systems that support [primary-selection-unstable-v1](https://wayland.app/protocols/primary-selection-unstable-v1) or the older Gtk primary selection protocol.
