fnkeysh
=======
A skeleton bash-file, intended to be used to write project specific shell-subroutines (e.g. build) that are called by some arbitrary client (e.g. your favorite window manager) that binds those subroutines to keys (e.g. the function key row).


## Usage
Copy the skeleton bash-file into the root of your project folder, replace the NAME variable as wanted and extend the script by adding functions named after the key they should be binded to at the top, like so:

```sh
F1() {
   cat /dev/null
}
``` 

Activate the script by calling it once with the "hook" argument (e.g. # ./.fnkeysh hook).

## Bindings
Merely call the ".fnkey" file in your HOME directory with the name of the key to be invoked as argument. 

### Examples:
For i3wm, add these to your config:
```sh
#FnKeys
bindsym $mod+F1 exec ~/.fnkeys F1
bindsym $mod+F2 exec ~/.fnkeys F2
bindsym $mod+F3 exec ~/.fnkeys F3
bindsym $mod+F4 exec ~/.fnkeys F4
bindsym $mod+F5 exec ~/.fnkeys F5
bindsym $mod+F6 exec ~/.fnkeys F6
bindsym $mod+F7 exec ~/.fnkeys F7
bindsym $mod+F8 exec ~/.fnkeys F8
```

For awesome-wm, add these to your rc.lua:
```lua
    -- FnKeys
    awful.key({ modkey },           "F1",    function () awful.util.spawn_with_shell("~/.fnkey F1") end),
    awful.key({ modkey },           "F2",    function () awful.util.spawn_with_shell("~/.fnkey F2") end),
    awful.key({ modkey },           "F3",    function () awful.util.spawn_with_shell("~/.fnkey F3") end),
    awful.key({ modkey },           "F4",    function () awful.util.spawn_with_shell("~/.fnkey F4") end),
    awful.key({ modkey },           "F5",    function () awful.util.spawn_with_shell("~/.fnkey F5") end),
    awful.key({ modkey },           "F6",    function () awful.util.spawn_with_shell("~/.fnkey F6") end),
    awful.key({ modkey },           "F7",    function () awful.util.spawn_with_shell("~/.fnkey F7") end),
    awful.key({ modkey },           "F8",    function () awful.util.spawn_with_shell("~/.fnkey F8") end),
```

License
=======
I, the copyright holder of this work, release this work into the public domain. This applies worldwide.
In some countries this may not be legally possible; if so:
I grant anyone the right to use this work for any purpose, without any conditions, unless such conditions are required by law.
