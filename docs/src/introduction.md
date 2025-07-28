# Ewwii - Widgets made better

Ewwii (Elkowars Wacky Widgets Imporved Interface) is a fork of Elkowars Wacky Widgets which is a standalone widget system made in [Rust](https://www.rust-lang.org/) that allows you to implement your own, dynamic custom widgets in any window manager.

Configured in rhai and themed using CSS, it is easy to customize, is dynamic and provides all the flexibility you need!

## Installation

### Prerequisites

- rustc
- cargo

Additionally, eww requires some dynamic libraries to be available on your system. The exact names of the packages that provide these may differ depending on your distribution. The following list of package names should work for arch linux:

<details>
<summary><strong>Packages</strong></summary>

<ul>

<li>gtk3 (<code>libgdk-3</code>, <code>libgtk-3</code>)</li>
<li>gtk-layer-shell <em>(only on Wayland)</em></li>
<li>pango (<code>libpango</code>)</li>
<li>gdk-pixbuf2 (<code>libgdk_pixbuf-2</code>)</li>
<li>libdbusmenu-gtk3</li>
<li>cairo (<code>libcairo</code>, <code>libcairo-gobject</code>)</li>
<li>glib2 (<code>libgio</code>, <code>libglib-2</code>, <code>libgobject-2</code>)</li>
<li>gcc-libs (<code>libgcc</code>)</li>
<li>glibc</li>

</ul>
</details>

(Note that you will most likely need the -devel variants of your distro's packages to be able to compile eww.)

## Building

Once you have the prerequisites ready, you're ready to install and build eww.

**First clone the repo:**

```bash
git clone https://github.com/byson94/ewwii
```

```bash
cd eww
```

**Then build:**

```bash
cargo build --release --no-default-features --features x11
```

**NOTE:** When you're on Wayland, build with:

```bash
cargo build --release --no-default-features --features=wayland
```

## Running eww

Once you've built it you can now run it by entering:

```bash
cd target/release
```

Then make the Eww binary executable:

```bash
chmod +x ./eww
```

Then to run it, enter:

```bash
./eww daemon
./eww open <window_name>
```
