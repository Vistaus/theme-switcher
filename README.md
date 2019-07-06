# theme-switcher
Switch dark/light GTK theme automatically during day/night

### Prerequisites

```bash
sudo dnf install python3-gobject gtk3
sudo cp org.theme-switcher.gschema.xml /usr/share/glib-2.0/schemas/
sudo glib-compile-schemas /usr/share/glib-2.0/schemas/
```

### Install

Fedora:

```bash
sudo dnf copr enable atim/theme-switcher -y && sudo dnf install theme-switcher -y
```

### Run GUI version

```bash
theme-switcher-gui.py
```

### Run CLI version

#### Automatically

* Enable

```bash
systemctl --user enable --now theme-switcher-auto.timer
```

* Disable

```bash
systemctl --user disable --now theme-switcher-auto.timer
```

#### Manually

```
theme-switcher-manual
```

### Configure

You need to setup your light/dark profiles in gnome-terminal in order to switch terminal themes automatically. Configure them by edit:

```bash
sudoedit /usr/bin/theme-switcher-auto.sh
```
