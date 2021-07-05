# Kaunas
Openbox Window Manager theme that seeks for easy and modern window navigation in today's OS design. Initially was designed for LXQT desktop environment to make it more modern and comply with the modern OS design. Inspired by Windows® 11 Fluent design.
<br></br>
<br>
![alt text](https://i.imgur.com/qlTsatZ.png)
</br>
\* Theme preview with picom compositor fork (https://github.com/ibhagwan/picom)
<br></br>
## Installation
Download this repository via repository button above or clone it via this command inside CLI: ``git clone https://github.com/Dovias/Kaunas/``. After that, copy the folder inside ``~/.themes/`` directory. In order to enable this theme inside <b>LXQT desktop environment</b>, go to ``LXQT Settings/Openbox Settings/Theme/`` and select the <b>Kaunas</b> theme.
### Enabling rounded corners
Openbox does not support rounded corners by default, due to these technical limitations, some elements like menu list boxes are not rounded, but in order to compensate this, you can use forked picom compositor by ibhahwan (https://github.com/ibhagwan/picom) which provides support for your GPU to render your GUI and to round corners and blur windows. This small tutorial is only suited for LXQT since this theme was only designed for modernising LXQT and not other desktop environments, but the process should be somewhat similiar.
- On <b>Arch Linux</b> based distributions, you can use https://aur.archlinux.org/packages/picom-ibhagwan-git/ <b>AUR</b> repository to install picom compositor. If you don't know how to install Arch User Repository packages, follow the instructions provided here: https://dev.to/nabbisen/installing-aur-packages-bdf. 
- On <b>Debian</b> and other based distributions unfortunately you need to build the source code of the display compositor yourself. Seek for build information here: https://github.com/yshui/picom/blob/next/README.md#build

After the installation of picom, add the installed compositor inside autostart daemon by going into ``LXQT Settings/Session settings/Autostart/`` and adding the new autostart application with command ``picom``. Then, copy the default picom configuration file from ``/etc/xdg/`` directory to ``~/config/`` location and set ``round-corners=0`` and ``round-radius`` options to ``round-corners=1``, ``round-radius=25.0`` and save the file. Restart your PC. For more information regarding the compositor, seek the information here: https://wiki.archlinux.org/title/Picom. I suggest you take a look into its config, it could do much more than round corners, for example, it can add window shadows which are non-existant inside LXQT desktop environment. (This does not provide documentation for blurring and rounding corners since these are unofficial features added by the community, not by the maintainers themselves, although some git merges are being done right now.)
### What about the rounded corners patch for Openbox WM?
I am looking keen on that, but in the meantime, you need to use compositor to enable rounded corners. In the future, I will probably upload the updated theme, rather than betting on the compositor itself, since those patches would probably fix the issues with menu list graphical limitations.
### My menu bar and menu list fonts are different from the preview image. How to change it?
By default, Openbox WM uses different fonts to display text in menu bar and its list. Fonts inside Openbox Window Manager are separate and independent from the themes, so to change this in LXQT desktop environment you can go to ``LXQT Settings/Openbox Settings/Font`` and change ``Active window title``, ``Inactive window title`` and ``Menu item`` fonts to your choice. Font that is used in preview is ``Noto Looped Lao Medium``, since I think it closely resembles the ``Segoe UI`` font which is used for display text inside Microsoft Windows® operating system. 
### While right clicking on the menu bar, menu list displayed is small. What went wrong there?
Probably, you have high DPI monitor that causes this issue. Since you have more pixels to display the menu list, it would appear smaller, since pixels on your monitor are arranged in more compact way. To compensate this, you can increase font size for menu bars via ``LXQT Settings/Openbox Settings/Font`` and choosing your size of choice depending on your monitor resolution.
## This was made possible by
- NotEnoughDanger (For his recreation of Windows® style minimize, maximize, iconify buttons, https://www.pling.com/p/1084968/)
- Dovias
<br>
Made with ♥ in Lithuania 🇱🇹
</br>
