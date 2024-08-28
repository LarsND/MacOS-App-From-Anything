# MacOS-App-From-Anything

This script automates the process of creating a macOS application bundle, for example, for a Java application, including generating or using an existing `.icns` icon file, setting up the `Info.plist`, and compiling an AppleScript to launch the application.

## Prerequisites

- macOS
- `sips` (Scriptable Image Processing System)
- `iconutil` (for converting iconsets to `.icns` files)

## Usage

1. **Edit the script for your application:**

2. **Run the script:**

    ```bash
    ./TEMPLATE-APP-BUILDER.sh
    ```

3. **Follow the prompts:**

    - The script will ask if there is an existing `.icns` file. If yes, provide the path to the file.
    - If no, the script will ask if you want to generate a `.icns` file from an image. If yes, provide the name of the image file (e.g., `icon.png`).

4. **The script will:**

    - Generate the necessary icon sizes and convert them to a `.icns` file if needed.
    - Create the application bundle directory structure.
    - Generate and compile an AppleScript to launch the application.
    - Modify the `Info.plist` file with the necessary information.
    - Copy the icon and additional resources into the application bundle.

## Example

```bash
$ ./TEMPLATE-APP-BUILDER.sh
Is there an existing .icns file? (y/n): n
Do you want to generate a .icns file from an image? (y/n): y
Enter the name of the icon (with extension, e.g., icon.png): myicon.png
```

## Files and Directories

- `TEMPLATE-APP-BUILDER.sh`: The main script.
- `Example Java App Name.app`: The generated macOS application bundle.
- `main.scpt`: The temporary AppleScript file (deleted after compilation).

## Notes

- Ensure that the image file used to generate the `.icns` file is in the same directory as the script or provide the full path to the image file.
- The script assumes the application file (`jd-gui.jar` in this case) and additional resources are located in the `app-dir` directory.

## License

This project is licensed under the GPLv3 License.

## Author

LarsND

© 2024 LarsND