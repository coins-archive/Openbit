
Debian
====================
This directory contains files used to package Openbitd/Openbit-qt
for Debian-based Linux systems. If you compile Openbitd/Openbit-qt yourself, there are some useful files here.

## Openbit: URI support ##


Openbit-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install Openbit-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your Openbitqt binary to `/usr/bin`
and the `../../share/pixmaps/Openbit128.png` to `/usr/share/pixmaps`

Openbit-qt.protocol (KDE)

