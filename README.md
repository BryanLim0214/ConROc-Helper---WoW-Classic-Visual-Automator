# WoW Classic Rotation Helper

![WoW Classic Rotation Helper Logo](logo.png) A user-friendly application designed to assist World of Warcraft Classic players by automatically executing keybinds based on visual spell proc or rotation helper addon recommendations (like ConROc). It monitors a specific area of your screen for spell icons and presses the corresponding key when a configured spell is detected.

**Disclaimer:** Using automation tools like this may violate World of Warcraft's Terms of Service and could lead to account suspension or ban. **Use this software responsibly and at your own risk.** The developer is not responsible for any consequences resulting from its use.

## Features

* **Visual Spell Detection:** Monitors a user-defined screen region using OpenCV.
* **GUI Configuration:** Easy-to-use interface built with Tkinter for managing spells and settings.
* **Spell & Keybind Mapping:** Add spell icons and link them to their corresponding in-game keybinds.
* **Region Selection Tool:** Visually select the screen area to monitor.
* **Image Capture Tool:** Capture spell icons directly from your screen.
* **Customizable Detection:** Adjust match threshold and minimum spell duration/repetition behavior.
* **Global Hotkey:** Start and stop detection using a configurable hotkey (Default: `Ctrl+Shift+X`).
* **Persistent Settings:** Saves your spell list, detection area, and settings to a JSON file (`spell_config.json` by default).
* **Notifications:** Provides desktop notifications for status changes (Start/Stop, Save, etc.).
* **Monitoring Tab:** View live detection logs, status, and basic statistics.

## Screenshot

![Screenshot of WoW Classic Rotation Helper](link/to/your/screenshot.png)

## Installation

### Using the Executable (.exe)

1.  Download the latest `.exe` file from the [Releases](link/to/your/releases) page of this repository.
2.  Place the `.exe` file in a folder of your choice. Necessary assets like `logo.png` or `icon.ico` should ideally be in the same folder if they are not bundled *within* the exe by PyInstaller.
3.  No installation is required. Simply double-click the `.exe` file to run the application.

### Running from Source

1.  **Prerequisites:**
    * Python 3.x installed.
    * Git installed (optional, for cloning).
2.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(You will need to create a `requirements.txt` file containing:*
    ```
    opencv-python
    numpy
    pyautogui
    keyboard
    Pillow
    ```
    *)*
4.  **Run the Application:**
    ```bash
    python your_main_script_name.py
    ```
    *(Replace `your_main_script_name.py` with the actual name of the Python file you provided).*

## How to Use

1.  **Launch the Application:** Run the `.exe` or the Python script.
2.  **Configure Detection Area:**
    * Go to the **Detection Settings** tab.
    * Click the **Select Area** button. Your screen will dim slightly.
    * Click and drag a rectangle around the specific area on your screen where your rotation helper addon (like ConROc) displays the **icon of the *next* recommended spell**. Make the selection reasonably tight around the icon area.
    * The X, Y, Width, and Height fields will update automatically.
    * (Optional) Click **Preview Area** to see a snapshot of what the application will monitor.
3.  **Add Your Spells:**
    * Go to the **Spells** tab.
    * Click **Add New**.
    * **Spell Name:** Enter a descriptive name (e.g., "Fireball", "Heroic Strike").
    * **Keybinding:** Enter the exact keybind assigned to this spell on your WoW action bar (e.g., `1`, `f1`, `ctrl+5`, `shift+r`). Use the format recognized by the `keyboard` library (lowercase letters, modifiers like `ctrl`, `alt`, `shift` followed by `+`).
    * **Image Path:** You need an image of the spell icon *as it appears in the detection area*.
        * **Option A (Recommended): Capture:**
            1.  Click the **Capture** button.
            2.  Your screen will dim again. Click and drag a *tight* box around the spell's icon *within the game or rotation addon's display area*.
            3.  A "Save As" dialog will appear. Save the captured image (e.g., `fireball_icon.png`). The path will be filled automatically.
        * **Option B: Browse:** Click **Browse...** and select an existing image file of the spell icon. Ensure the image is clear, well-cropped, and matches how it looks in the detection area.
    * An **Image Preview** will appear if the path is valid.
    * Click **Save Spell**.
4.  **Repeat Step 3** for all the spells you want the helper to recognize and use.
5.  **Adjust Settings (Optional):**
    * Go to the **Detection Settings** tab.
    * **Match Threshold:** Controls how closely the image must match (0.1 to 1.0). Higher values are stricter. Start around `0.7` or `0.8` and adjust if needed.
    * **Min Spell Duration:** How long (in seconds) the helper might keep pressing the keybind if the same spell icon remains detected. Helps handle spells that need to be "spammed" briefly.
    * **Toggle Hotkey:** Change the key combination used to start/stop detection globally.
    * Click **Save Settings** after making changes.
6.  **Save Configuration:**
    * Go back to the **Spells** tab.
    * Click **Save Config** to save your current spell list and settings to the default `spell_config.json`.
    * Use **Save As...** or **Load Config** to manage multiple configurations (e.g., for different characters or specs).
7.  **Start Detection:**
    * Go to the **Monitor** tab.
    * Click the **Start Detection** button.
    * Alternatively, press the configured **Toggle Hotkey** (default `Ctrl+Shift+X`) while the application is running (even if minimized).
    * You should see log messages appearing in the "Detection Log" when spells are detected and keys are pressed. Notifications may also appear.
8.  **Stop Detection:**
    * Click the **Stop Detection** button in the **Monitor** tab.
    * Or, press the **Toggle Hotkey** again.

## Configuration File (`spell_config.json`)

The application saves its settings in a `spell_config.json` file in the same directory. This file includes:

* `spells`: A list of your configured spells, each with its name, image path, and keybind.
* `detection_area`: The coordinates (x, y, width, height) of the monitored screen region.
* `threshold`: The image matching sensitivity.
* `min_spell_duration`: The duration setting for repeated key presses.
* `toggle_hotkey`: The global hotkey string.

You can manually edit this file, but it's generally easier to use the GUI. Back up this file to save your configuration.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for bugs or feature requests.

## License

This project is licensed under the [MIT License](LICENSE). ```

