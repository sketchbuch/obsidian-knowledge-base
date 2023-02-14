# Desktop Launchers

Information about Desktop Launchers, how to create them and get the icon visible in the app grid.

---

## Create Desktop File:

Create a .desktop file in `~/.local/share/applications`. 

```bash
[Desktop Entry]
Name=RClone Browser
Exec="/home/username/Some Path/rclone-browser.AppImage"
Icon=/home/username/Pictures/App\sIcons/rclone.png
comment=Sync cloud drives.
Type=Application
Terminal=false
Encoding=UTF-8
Categories=Utility;
```

[Source](https://www.how2shout.com/linux/how-to-create-desktop-shortcut-for-an-appimage/)

Name the desktop file the same as the *running* app name to be able to add it to the dash as a favourite app.