# windows-desktop-switcher-Asamai-version
My custom config file of [windows desktop switcher](https://github.com/pmb6tz/windows-desktop-switcher). 
Changes in the config file:

```
SetCapsLockState, AlwaysOff
```
to always keep the CapsLock key off and stop the annoying notification whenever the CapsLock key in pressed.

```
; The following hotkeys only work when CapsLock is physically held down
#If GetKeyState("CapsLock", "P")

; CapsLock + Number -> Switch Desktop
1::switchDesktopByNumber(1)
2::switchDesktopByNumber(2)
3::switchDesktopByNumber(3)
4::switchDesktopByNumber(4)
5::switchDesktopByNumber(5)
6::switchDesktopByNumber(6)
7::switchDesktopByNumber(7)
8::switchDesktopByNumber(8)
9::switchDesktopByNumber(9)

; "+" represents the Shift key. So +1 means Shift+1.
+1::MoveCurrentWindowToDesktop(1)
+2::MoveCurrentWindowToDesktop(2)
+3::MoveCurrentWindowToDesktop(3)
+4::MoveCurrentWindowToDesktop(4)
+5::MoveCurrentWindowToDesktop(5)
+6::MoveCurrentWindowToDesktop(6)
+7::MoveCurrentWindowToDesktop(7)
+8::MoveCurrentWindowToDesktop(8)
+9::MoveCurrentWindowToDesktop(9)

; Closes the conditional block
#If
```
so I can do `CapsLock + n` to move to `Desktop n` and `CapsLock + Shift + n` to move current window to `Desktop n`.
