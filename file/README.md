<div align="center">
<img src="https://github.com/cleragui/pypi/blob/main/image/logo-with-name.png?raw=true">
</div>

## **Clera — GUI Development with Python** 🐍

![PyPI Downloads](https://static.pepy.tech/badge/clera)
![PyPI Version](https://img.shields.io/pypi/v/clera)
![Python Versions](https://img.shields.io/pypi/pyversions/clera)
![License](https://img.shields.io/pypi/l/clera)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)

---

Clera is a Python GUI framework that lets you build desktop applications quickly and simply — with a low learning curve and minimal boilerplate.

<br>

> **NOTE:** Clera is currently in **developer beta**. Core features are stable and undergoing broader testing before the full public release. To participate in testing or get help, reach out at eirasmx@pm.me

<br>

## **✦ THE BASICS**

### **Installation**

```bash
pip install clera
```

> Requires Python 3.7+ and PySide6.

<br>

### **Your First Window**

Every Clera application starts with a `Window`. This is the skeleton of any GUI built with Clera:

```python
from clera import Window

window = Window()
# Add your widgets and layouts here
window.run()
```

**Output:**

![Window](https://github.com/cleragui/pypi/blob/main/image/window.png?raw=true)

> **" Why Complicate Simplicity? "**

<br>

### **Adding Widgets**

Clera widgets are simple, readable Python objects. Here's a basic example with a label and a button:

```python
from clera import Window, Label, Button, Box

def on_click():
    print("Hello from Clera!")

window = Window()
window.add(
    Box([
        Label("Welcome to Clera 👋"),
        Button("Click Me", func=on_click)
    ])
)
window.run()
```

<br>

### **Layouts**

Use `Box` for vertical/horizontal stacking and `Grid` for grid-based arrangements:

```python
from clera import Window, Box, Grid, Label

window = Window()
window.add(
    Grid([
        [Label("A"), Label("B")],
        [Label("C"), Label("D")]
    ])
)
window.run()
```

<br>

### **Styling**

Clera uses a CSS-like styling system with its own tag aliases. You can apply styles inline or link an external `.cx` stylesheet:

```python
window = Window(style="background: #1e1e1e;")
```

<br>

## **✦ TOOLS**

Clera ships with two built-in command-line tools:

| Command | Description |
|---|---|
| `clera-editor` | Launch the Clera Style Editor — itself built with Clera |
| `clera-deploy` | Package your Clera app into a standalone executable |

Run either from your terminal or command prompt after installing Clera.

<br>

## **✦ PLATFORMS**

### **Hardware**
- Desktop and Laptops

### **OS**
- 🪟 Windows
- 🍎 macOS
- 🐧 Linux

<br>

> **📖 Docs:** Visit [https://clera.readthedocs.io](https://clera.readthedocs.io) for full documentation and guides.

<br>

---

<br>

### **RELEASE NOTES**

**v0.3.0 (2026-04-21) - Developer Beta**

- Splitter widget with live resize and collapsible panes (**added**)
- TreeView widget with drag-and-drop, branch editing, and sorting (**added**)
- SpinBox widget with integer and float modes, prefix and suffix support (**added**)
- `cursor()` element with custom image and type support (**added**)
- Context menu support to Image, List, Select, and Table widgets (**added**)
- `font()` helper for loading external font files (**added**)

<br>

- `Box()` and `Grid()` now accept `css`, `size`, `fixed_size`, `min_size`, `max_size`, and `id` parameters (**added**)
- `Column()` now accepts `margin` and `spacing` parameters (**added**)
- `tab()` now accepts an `id` parameter (**added**)
- `Window.run()` now accepts `instance` and `child` parameters for multi-window support (**added**)
- `Window.fullscreen()` method (**added**)
- `Window` now accepts `alignment`, `radius`, and `hide_cursor` parameters (**added**)
- Rounded window mask with `radius` parameter and live resize support (**added**)

<br>

- Multi-window management via internal window registry (**added**)
- `ensure_window_root()` utility for multi-window context resolution (**added**)
- CSS scoping improvements and alias table pre-compilation for faster parsing (**improved**)
- `MenuBar` class renamed from `Menubar` for consistency (**changed**)

<br>

- Custom exception classes now carry docstrings (**improved**)
- `blob` and `null` database types expanded with proper class bodies (**improved**)
- Clera Editor layout stabilised; editor auto-runs on import (**fixed**)

<br>

---
