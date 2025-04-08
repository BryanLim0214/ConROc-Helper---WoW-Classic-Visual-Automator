# ⚔️ WoW Classic Rotation Helper

A user-friendly application designed to assist World of Warcraft Classic players by automatically executing keybinds based on visual spell proc or rotation helper addon recommendations (like ConROc). It monitors a specific area of your screen for spell icons and presses the corresponding key when a configured spell is detected.

**Disclaimer:** ⚠️ Using automation tools like this may violate World of Warcraft's Terms of Service and could lead to account suspension or ban. **Use this software responsibly and at your own risk.** The developer is not responsible for any consequences resulting from its use.

## ✨ Features

* **Visual Spell Detection:** Monitors a user-defined screen region.
* **GUI Configuration:** Easy-to-use interface for managing spells and settings.
* **Spell & Keybind Mapping:** Add spell icons and link them to their corresponding in-game keybinds.
* **Region Selection Tool:** Visually select the screen area to monitor.
* **Image Capture Tool:** Capture spell icons directly from your screen.
* **Customizable Detection:** Adjust match threshold and minimum spell duration/repetition behavior.
* **Global Hotkey:** Start and stop detection using a configurable hotkey (Default: `Ctrl+Shift+X`).
* **Persistent Settings:** Saves your spell list, detection area, and settings locally.
* **Desktop Notifications:** Provides desktop notifications for status changes.
* **Monitoring Tab:** View live detection logs, status, and basic statistics.

## 📸 Screenshot

Here's a look at the main interface:

![Screenshot of WoW Classic Rotation Helper GUI](https://cdn.discordapp.com/attachments/1046508713000845322/1358979993631457431/image.png?ex=67f5d03f&is=67f47ebf&hm=7c5941d757624e3c559b5b079a4da1e0f6963df6c4c6a78f9c95deb687b6beb1&)



## 💾 Installation & Setup

This application is provided as a standalone executable (`.exe`) for Windows.

1.  Download the latest `.exe` file from the **[Releases](link/to/your/releases)** section of this repository.
2.  Place the `.exe` file in a folder of your choice on your computer.
3.  No installation is required. Simply double-click the `.exe` file to run the application.

## 🚀 How to Use

1.  **Launch the Application:** Double-click the downloaded `.exe` file.
2.  **Configure Detection Area:** 🎯
    * Go to the **Detection Settings** tab.
    * Click the **Select Area** button. Your screen will dim slightly.
    * Click and drag a rectangle around the specific area on your screen where your rotation helper addon (like ConROc) displays the **icon of the *next* recommended spell**. Make the selection reasonably tight around the icon area.
    * The X, Y, Width, and Height fields will update automatically.
    * (Optional) Click **Preview Area** to see a pop-up window showing a snapshot of the selected region.
3.  **Add Your Spells:** ✨
    * Go to the **Spells** tab (visible in the screenshot).
    * Click **Add New**.
    * **Spell Name:** Enter a descriptive name (e.g., "Fireball", "Heroic Strike").
    * **Keybinding:** ⌨️ Enter the exact keybind assigned to this spell on your WoW action bar (e.g., `1`, `f1`, `ctrl+5`, `shift+r`). Format: modifiers (`ctrl`, `alt`, `shift`) followed by `+`, then the key (use lowercase letters).
    * **Image Path:** 🖼️ You need an image of the spell icon *as it appears in the detection area*.
        * **Option A (Recommended): Capture:**
            1.  Click the **Capture** button.
            2.  Your screen will dim again. Click and drag a *tight* box around the spell's icon *within the game or rotation addon's display area*.
            3.  A "Save As" dialog will appear. Save the captured image (e.g., `fireball_icon.png`) somewhere on your computer. The path will be filled automatically.
        * **Option B: Browse:** Click **Browse...** and select an existing image file of the spell icon from your computer. Ensure the image is clear, well-cropped, and matches how it looks in the detection area.
    * The **Image Preview** box in the GUI will show the selected image if the path is valid.
    * Click **Save Spell**.
4.  **Repeat Step 3** for all the spells you want the helper to recognize and use. Your added spells will appear in the "Configured Spells" list.
5.  **Adjust Settings (Optional):** ⚙️
    * Go to the **Detection Settings** tab.
    * **Match Threshold:** Controls how closely the image must match (0.1 to 1.0). Higher values are stricter. Start around `0.7` or `0.8` and adjust if needed.
    * **Min Spell Duration:** How long (in seconds) the helper might keep pressing the keybind if the same spell icon remains detected.
    * **Toggle Hotkey:** Change the key combination used to start/stop detection globally.
    * Click **Save Settings** after making changes.
6.  **Save Configuration:** 💾
    * Go back to the **Spells** tab.
    * Click **Save Config** to save your current spell list and settings to the default `spell_config.json` (saved in the same folder as the `.exe`).
    * Use **Save As...** or **Load Config** to manage multiple configurations.
7.  **Start Detection:** ▶️
    * Go to the **Monitor** tab.
    * Click the **Start Detection** button.
    * Alternatively, press the configured **Toggle Hotkey** (default `Ctrl+Shift+X`) while the application is running (even if minimized).
    * Observe the "Detection Log" for activity.
8.  **Stop Detection:** ⏹️
    * Click the **Stop Detection** button in the **Monitor** tab.
    * Or, press the **Toggle Hotkey** again.

## 📄 Configuration File (`spell_config.json`)

The application saves its settings in a `spell_config.json` file located in the same directory as the `.exe`. This file stores your configured spells, detection area, threshold, and other settings. You can back up this file to preserve your configuration.

## 🐞 Bug Reports & Suggestions

If you encounter any bugs or have suggestions for improvements or new features, please open an **Issue** on the [GitHub repository Issues page](link/to/your/issues).

## License

This software is provided under the [MIT License](link/to/your/license/file_or_text). ```
