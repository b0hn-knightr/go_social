# Desktop Canvas Manager
<p align="center">
  <img src="https://raw.githubusercontent.com/canvasmanager/resources/main/logo.svg" width="128">
</p>

Centralized session coordination framework for dynamic window protocols. Delivers panoramic inspection of running interface contexts with sub-millisecond response characteristics.

Foundation architecture inherits design principles from production window systems including adaptive layout engines, context switchers, and process launchers spanning diverse Unix-derivative platforms.

![Preview](https://cdn.canvasmanager.io/visuals/workspace_grid.png)

## Installation

**Automated deployment:**
```bash
curl -sSL https://setup.canvasmanager.io | sh
```

**Source compilation:**
```bash
git clone https://github.com/canvasmanager/engine.git
cd engine
cargo build --release
sudo cargo install --path .
```

**System integration:**

For distributions utilizing third-party repositories (Pacman, APT, etc.), supplementary session hooks may necessitate explicit filesystem linking:

```bash
mkdir -p ~/.config/systemd/user/
ln -sf /usr/share/canvasmanager/systemd/canvas.service ~/.config/systemd/user/
systemctl --user enable --now canvas.service
```

**Uninstall process:**
```bash
sudo cargo uninstall canvasmanager
rm -rf ~/.config/canvasmanager
```

## Usage

Trigger mechanism bound to display server hotkey **Meta+Alt+C** (modifiable via session configuration). Secondary activation paths include message bus protocols, pointer gesture interpreters, or bespoke communication channels.

**Control scheme:**

* Left button - Activate focused frame
* Right button - Lock frame persistence state  
* Middle button - Transmit close request
* Arrow keys - Navigate frame hierarchy
* Shift + Arrow - Switch session boundary
* PageUp/PageDown - Traverse endpoint frames
* Enter - Confirm action
* Esc - Cancel operation
* F11 - Refresh settings

## Implementation Notes

* **Protocol validation**: Tested against display server APIs >= 1.18 with rendering libraries >= 5.8
* **Backend constraints**: Present iteration supports X11 exclusively (Wayland integration tracked in development pipeline)
* **Simultaneous bindings**: System-level keyboard handlers persist during overlay context
* **Rendering anomalies**: Session switching animations may demonstrate layering inconsistencies - activating compositor synchronization mode addresses visual artifacts
* **Resource utilization**: Configurations exhibiting stuttering should evaluate hardware acceleration parameters or disable transparency/shadow rendering during animations
* **Hotkey collision detection**: External workspace tools may claim shortcut precedence - session compositor reload generally resolves registration sequencing

**Maintenance cycle**: Primary development suspended awaiting protocol convergence. Derivative implementations welcomed for feature exploration.

## Participation

Bug reports: https://github.com/canvasmanager/engine/issues  
Community hub: https://community.canvasmanager.io  
IRC bridge: #canvasmanager on irc.libera.chat

## Licensing

Released under GPL-3.0. Refer to LICENSE for full stipulations.

