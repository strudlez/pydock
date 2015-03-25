## What is PyDock? ##
Pydock is a simple dock bar that tracks open windows under Windows XP and Vista. The Executable has no dependencies and runs right out of the box. It aims to be configurable, portable and light weight. PyDock is still under _heavy_ development (alpha code) and thus may have a few bugs.

Source can be found at http://pydock.googlecode.com/svn/trunk/.

9/16/2007 - Small Bugfix for Window Detection

### CURRENT 0.8 ###
![http://alexsmk.googlepages.com/Pydock.JPG/Pydock-full.jpg](http://alexsmk.googlepages.com/Pydock.JPG/Pydock-full.jpg)

**Current Specs (0.8):**

  * Tracks Open Windows
  * Allows Minimize, Maximize and Restore
  * Transparency
  * Remove/Restore Taskbar
  * Add Launchers for Applications
  * Window Previews
  * Written in Python with PyWin32


**Note: In V.0.8 Settings are stored in the auto-generated _conf.txt_, You can set transparency but changing the float on line 1 to something between 1.0 & 0.0. If you mess up your settings somehow delete _conf.txt_ when PyDock is not running. If anyone wants to help out with this project E-mail me**

**TODO for V.0.9:**
  * Port UI to WX
  * Add shaped windows
  * Get DIB from hdc (Better Window previews)
  * Fix minor window detection bug (Fixed)
  * Add better Settings Configuration
  * Improve Transparency

_Anyone know how to use SendMessage + WM\_PRINT and then get the bitmap from the hdc? Drop me a note_

```
  hdc = win32gui.CreateCompatibleDC(hdcSrc)
  hBitmap = win32gui.CreateCompatibleBitmap(hdcSrc, 512,324)
  win32gui.SelectObject(hdc, hBitmap)
  destHDC = hdcDestH.GetSafeHdc()
```