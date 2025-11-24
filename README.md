MiddleClicker

A lightweight, open-source macOS utility that turns Fn + Click (or Fn + Tap) into a Middle Click.

Designed specifically for 3D applications like Blender, Maya, and CAD software where holding the middle mouse button is required to pan or rotate the viewport.


Features

🖱️ Fn + Click = Middle Click: Hold Fn and click dragging on the trackpad to emulate a middle-mouse drag.

🤏 Native Trackpad Support: Works with physical clicks and simulates the middle button "hold" state perfectly.

⚡️ Lightweight: Written in Swift, runs as a background accessory (no Dock icon).

🔓 Open Source: Verify the code yourself; no hidden scripts.

Installation

Option 1: Download the App

Go to the Releases page.

Download MiddleClicker_Installer.dmg.

Open the DMG and drag MiddleClicker into your Applications folder.

First Run: Right-click the app and select Open (since this is an unsigned open-source app).

Grant Accessibility Permissions when prompted.

Option 2: Build from Source

If you prefer to compile it yourself:

Clone this repository:

git clone [https://github.com/yourusername/MiddleClicker.git](https://github.com/fordft168/MiddleClicker.git)
cd MiddleClicker


Run the build script:

chmod +x build.sh
./build.sh


The compiled MiddleClicker_Installer.dmg will be in the project folder.

How it works

This app uses a CGEventTap to intercept leftMouseDown events. If the Fn key is detected as a modifier, it swallows the left click and generates a otherMouseDown (Button 3) event instead. It tracks the drag state to allow for continuous middle-mouse dragging operations.

License

MIT License
