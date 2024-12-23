
# Open and Close Discord RPC for Apple Music Automatically 🎵

This batch script helps manage and launch two applications: **Apple Music** and **AMWin-RichPresence**, providing a convenient way to automate their startup and ensure they are running only when needed. It checks if either or both applications are already running and performs actions accordingly:

1. If neither application is running, it starts both.
2. If one application is running, it starts the other.
3. If both applications are running, it does nothing.

## Features ✨

- **Smart Detection**: Automatically checks for running instances of the applications.
- **Efficient Launching**: Starts only the required applications based on their current state.
- **Simple Setup**: Easy-to-use batch script for seamless management.

## Prerequisites 🛠️

- Windows OS
- Installed versions of:
  - **Apple Music**: Usually Located at(Check for your locations) `C:\Program Files\WindowsApps\AppleInc.AppleMusicWin_1.1282.14849.0_x64__nzyj5cx40ttqa\AppleMusic.exe`
  - **AMWin-RichPresence**: Download it from [AMWin-RP Releases](https://github.com/PKBeam/AMWin-RP/releases)

## Installation 📥

1. Download the bat file from [Releases](https://github.com/Swoyamjeetcodes/Apple-Music-Discord-RPC-modified/releases).
2. Open the script file `Apple Music.bat` in a text editor.
3. Verify and update the paths to `AppleMusic.exe` and `AMWin-RichPresence.exe` **(IMPORTANT)**.

To update the paths for the applications:
1. Open `Apple Music.bat` in a text editor.
2. Modify the following lines to reflect the correct paths for your system:
   ```batch
   set "appleMusicPath=C:\Path\To\AppleMusic.exe"
   set "amRichPresencePath=C:\Path\To\AMWin-RichPresence.exe"
   ```

## Usage 🚀

1. Double-click the `Apple Music.bat` file to run the script.
2. The script will automatically detect and launch the applications as needed.

### If You Want to Pin to Start 📌

1. Create a shortcut for the batch file.
2. Set the target of the shortcut to:
   ```cmd
   cmd.exe /C "path-to-your-batch"
   ```
3. You can also rename the shortcut to "Apple Music" and assign it an icon file (.ico) similar to Apple Music's logo for a polished look.

## Troubleshooting ❓

- **Issue**: The script does not start the applications.
  - **Solution**: Ensure the paths to the executables are correct and the applications are installed in the specified locations.
- **Issue**: The script does not detect running applications.
  - **Solution**: Confirm the process names (`AppleMusic.exe`, `AMWin-RichPresence.exe`) match the actual process names in Task Manager.

## Contributing 🤝

Feel free to submit issues or pull requests to enhance the functionality of this script.

## License 📄

This project is licensed under the MIT License. See the LICENSE file for details.
