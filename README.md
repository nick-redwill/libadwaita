# Adwaita

Building blocks for modern GNOME applications.

## Attention

This is a fork of [GNOME Libadwaita](https://github.com/GNOME/libadwaita) project with the goal 
of improving custom themes support and specifically addressing dynamic color scheme (dark/light)
changing issue.

Please keep in mind that this was tested only in **GNOME 48.1**. If you have different Gnome version
you can clone, compile and test on specific apps (see Usage) before installing globally. Even so
do system-wide installation **on your risk**.

For custom themes to be applied you must set these environment variables:
```
export GTK_THEME_LIGHT=Adwaita
export GTK_THEME_DARK=Adwaita-Dark
```

Or if you want to apply theme only to a specific app:
```
GTK_THEME_LIGHT=Adwaita GTK_THEME_DARK=Adwaita-Dark nautilus
```

## License

Libadwaita is licensed under the LGPL-2.1+.

## Building

We use the Meson (and thereby Ninja) build system for libadwaita. The quickest
way to get going is to do the following:

```sh
meson setup _build
ninja -C _build
ninja -C _build install
```

For build options see [meson_options.txt](./meson_options.txt). E.g. to enable documentation:

```sh
meson setup _build -Ddocumentation=true
ninja -C _build
```

## Usage

There's a C example:

```sh
_build/run _build/demo/adwaita-1-demo
```

## Documentation

The documentation can be found online
[here](https://gnome.pages.gitlab.gnome.org/libadwaita/doc/).

## Getting in Touch

Matrix room: [#libadwaita:gnome.org](https://matrix.to/#/#libadwaita:gnome.org)

