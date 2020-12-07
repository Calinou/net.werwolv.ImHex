# Flatpak for ImHex

## Installation

This Flatpak is available on
[Flathub](https://flathub.org/apps/details/net.werwolv.ImHex).
After following the [Flatpak setup guide](https://flatpak.org/setup/),
you can install it by entering the following command in a terminal:

```bash
flatpak install --user flathub net.werwolv.ImHex -y
```

Once the Flatpak is installed, you can run ImHex using your desktop environment's
application launcher.

## Updating

This Flatpak follows the latest stable ImHex version.
To update it, run the following command in a terminal:

```bash
flatpak update
```

## Limitations

- None known.

## Building from source

Install Git, follow the
[flatpak-builder setup guide](https://docs.flatpak.org/en/latest/first-build.html)
then enter the following commands in a terminal:

```bash
git clone --recursive https://github.com/flathub/net.werwolv.ImHex.git
cd net.werwolv.ImHex/
flatpak install --user flathub org.freedesktop.Sdk//20.08 -y
flatpak-builder --force-clean --install --user -y builddir net.werwolv.ImHex.yaml
```

If all goes well, the Flatpak will be installed after building. You can then
run it using your desktop environment's application launcher.

You can speed up incremental builds by installing [ccache](https://ccache.dev/)
and specifying `--ccache` in the flatpak-builder command line (before `builddir`).
