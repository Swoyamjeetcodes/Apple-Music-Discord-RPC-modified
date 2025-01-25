# Open and Close Discord RPC for Apple Music Automatically 🎵

This batch script helps manage and launch two applications: **Apple Music** and **AMWin-RichPresence**, providing a convenient way to automate their startup and ensure they are running only when needed. It checks if either or both applications are already running and performs actions accordingly:

1. If neither application is running, it starts both.
2. If one application is running, it starts the other.
3. If both applications are running, it does nothing.

## Features ✨

- **Smart Detection**: Automatically checks for running instances of the applications.
- **Efficient Launching**: Starts only the required applications based on their current state.
- **UWP Support**: Utilizes the `AppUserModelID` to properly launch UWP (Microsoft Store) applications like Apple Music.
- **Simple Setup**: Easy-to-use batch script for seamless management.

## Prerequisites 🛠️

- Windows OS
- Installed versions of:
  - **Apple Music** (Microsoft Store): Ensure it is installed from the Microsoft Store.
  - **AMWin-RichPresence**: Download it from [AMWin-RP Releases](https://github.com/PKBeam/AMWin-RP/releases).

## Installation 📥

1. Download the `.bat` file from [Releases](https://github.com/Swoyamjeetcodes/Apple-Music-Discord-RPC-modified/releases).
2. Open the script file `Apple Music.bat` in a text editor.
3. Update the path for **AMWin-RichPresence** to match your system:
   ```batch
   set "amRichPresencePath=C:\Path\To\AMWin-RichPresence.exe"
   ```

## Usage 🚀

1. Double-click the `Apple Music.bat` file to run the script.
2. The script will automatically detect and launch the applications as needed using the following logic:
   - If **both** Apple Music and AMWin-RichPresence are already running, the script exits without starting anything.
   - If **only one** of the applications is running, it starts the other.
   - If **neither** application is running, it starts both.
3. Apple Music is launched using its `AppUserModelID`, ensuring compatibility with its UWP nature.

### Launch via Shortcut 📌

1. Create a shortcut for the batch file.
2. Set the target of the shortcut to:
   ```cmd
   cmd.exe /C "path-to-your-batch"
   ```
3. Optionally, rename the shortcut to "Apple Music" and assign it an icon file (.ico) for a polished look.

## Troubleshooting ❓

- **Issue**: The script does not start Apple Music.
  - **Solution**: Ensure the correct `AppUserModelID` for Apple Music is used. To verify, run the following PowerShell command:
    ```powershell
    Get-StartApps | Where-Object { $_.Name -like "*Apple*" }
    ```
    Replace the ID in the script with the output for Apple Music if necessary.
- **Issue**: The script does not start AMWin-RichPresence.
  - **Solution**: Confirm the path to `AMWin-RichPresence.exe` is correct and the file exists in the specified location.
- **Issue**: The script does not detect running applications.
  - **Solution**: Check the process names (`AppleMusic.exe`, `AMWin-RichPresence.exe`) in Task Manager and ensure they match the ones in the script.

## Contributing 🤝

Feel free to submit issues or pull requests to enhance the functionality of this script.

## License 📄

This project is licensed under the MIT License. See the LICENSE file for details.
