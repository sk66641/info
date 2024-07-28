<h1 style="text-align: center">Info</h1> 
 
## To create a clickable shortcut that opens a website, you can create a `.desktop` file in Linux. A `.desktop` file is a standard way to create shortcuts in desktop environments like GNOME, KDE, and others.

Here’s how you can create a `.desktop` file to open a website:

1. **Create the `.desktop` File**

Use a text editor to create a new file with the `.desktop` extension. For example, create `example_website.desktop`:

```sh
nano ~/example_website.desktop
```

2. **Add the Following Contents to the File**

```ini
[Desktop Entry]
Version=1.0
Name=Example Website
Comment=Open Example Website
Exec=xdg-open https://www.example.com
Icon=web-browser
Terminal=false
Type=Application
Categories=Network;WebBrowser;
```

- `Name` is the name of the shortcut.
- `Comment` is a description of the shortcut.
- `Exec` is the command to execute, which opens the specified URL.
- `Icon` is the icon to display for the shortcut. You can specify a path to a custom icon if desired.
- `Terminal` should be `false` for GUI applications.
- `Type` should be `Application`.
- `Categories` help organize the shortcut in application menus.

3. **Make the `.desktop` File Executable**

```sh
chmod +x ~/example_website.desktop
```

4. **Move the File to a Suitable Location**

To make the shortcut available on your desktop or in your application menu, move the file to the appropriate directory:

- **For the desktop:**

```sh
mv ~/example_website.desktop ~/Desktop/
```

- **For application menu:**

```sh
mv ~/example_website.desktop ~/.local/share/applications/
```

### Example

Here’s a full example:

1. **Create the `.desktop` File:**

```sh
nano ~/example_website.desktop
```

2. **Add the Contents:**

```ini
[Desktop Entry]
Version=1.0
Name=Example Website
Comment=Open Example Website
Exec=xdg-open https://www.example.com
Icon=web-browser
Terminal=false
Type=Application
Categories=Network;WebBrowser;
```

3. **Make it Executable:**

```sh
chmod +x ~/example_website.desktop
```

4. **Move it to the Desktop:**

```sh
mv ~/example_website.desktop ~/Desktop/
```

Now you should have a clickable shortcut on your desktop that opens `https://www.example.com` in your default web browser when clicked.

## Opening a site using terminal
```
xdg-open https://github.com/sk66641
```

## Editing tools:
```
gedit, nano
```