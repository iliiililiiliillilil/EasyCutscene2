# EasyCutscence2
A lightweight and easy to use Roblox module for creating cinematic camera sequences. Supports any number of cameras, optional cinematic bars, smooth tweened movement, and automatic return to the player. Perfect for cutscenes, menus, and cinematic effects in Roblox games.

Perfect! Here’s a **polished, GitHub-ready README** for your EasyCutscene module. You can just paste this as `README.md` in your repo:

---

# EasyCutscene Module

**Author:** ill

A **lightweight and easy-to-use Roblox module** for creating cinematic camera sequences. Supports any number of cameras, optional cinematic bars, smooth tweened movement, and automatic return to the player. Perfect for cutscenes, menus, and cinematic effects in Roblox games.

---

## Features

* **Menu Camera Setup** – Set the camera to a static menu position for a specific duration.
* **Multi-Camera Cutscenes** – Pass a table of cameras to create cinematic sequences of any length.
* **Moveable or Static Cameras** – Smooth camera tweening or instant camera snaps.
* **Cinematic Bars** – Optional top and bottom bars for a movie-like feel, with fade-in and fade-out.
* **Automatic Return to Player** – Camera returns to the player after the cutscene.
* **Scalable & Reusable** – Works with any number of cameras, easy to integrate.

---

## Setup

1. Place the module in `ReplicatedStorage` or `ServerStorage`.
2. Ensure there’s an `Assets` folder in the module containing a `CinematicBar` GUI with `Frame` children for top and bottom bars.

---

## Usage

### Require the Module

```lua
local EasyCutscene = require(path_to_module)
```

---

### Menu Camera

```lua
local menuCamera = workspace.MenuCamera -- BasePart
EasyCutscene:addMainMenuCamera(menuCamera, 2) -- 2 seconds
```

* `camera` → BasePart representing the menu camera
* `duration` → optional, how long to stay on the menu camera

---

### Multi-Camera Cutscene

```lua
local cameras = {workspace.Camera1, workspace.Camera2, workspace.Camera3}
EasyCutscene:startCutscence(cameras, 3, true, true)
```

* `cameras` → table of BaseParts representing camera points
* `duration` → time each camera is shown in seconds
* `bars` → boolean, show cinematic bars or not
* `moveable` → boolean, smoothly tween camera or snap instantly

---

## Notes

* Ensure all cameras are `BasePart` objects.
* `CinematicBar` should have Frame children for top and bottom bars.
* Tweens use `Sine` easing for smooth cinematic motion.

---

## Optional Customization

* Change the color of cinematic bars by modifying the Frame in the `CinematicBar` GUI.
* You can adjust tween durations or easing styles in the module to fit your cutscene style.

---

## Example Folder Structure

```
EasyCutsceneModule
├── Assets
│   └── CinematicBar (ScreenGui)
│       ├── TopBar (Frame)
│       └── BottomBar (Frame)
├── EasyCutsceneModule.lua
└── README.md
```

---

## Future Improvements

* Add a **skip button** to allow players to skip cutscenes.
* Add **fade-to-black transitions** for more cinematic effect.
* Customize **tween durations and easing** per camera.
