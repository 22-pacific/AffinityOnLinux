# How to Set Up Wine for Affinity on Heroic Games Launcher (This should work with other launchers as long as you follow the same steps)

## 1. Install Desired Wine Version

Choose one of the following Wine versions:

- [**ElementalWarrior**](https://github.com/Twig6943/ElementalWarrior-wine-binaries/releases) (Recommended)
- [**Wine-TKG-Affinity**](https://github.com/daegalus/wine-tkg-affinity)

---

## 2. Install Heroic Games Launcher

Install Heroic Games Launcher using either **AppImage** or **Flatpak**.

---

## 3. Extract Wine Binaries

Extract the Wine binaries you downloaded earlier to Heroic Games Launcher’s Wine directory:

- **AppImage:** `/home/$USER/.config/heroic/tools/wine`
- **Flatpak:** `/home/$USER/.var/app/com.heroicgameslauncher.hgl/config/heroic/tools/wine`

---

## 4. Add Game in Heroic Games Launcher

1. Open Heroic Games Launcher and click on **Add Game**.
2. Name the game as you wish.
3. Set the Wine version to **ElementalWarriorWine** or **Wine-TKG-Affinity**.
4. Select the x64 setup `.exe` you downloaded from Affinity's website as the executable.
5. Click **Finish**.

---

## 5. Initialize the Wine Prefix

1. Run the setup file from Heroic to initialize the prefix.
   - It may crash. If it somehow runs successfully, close it manually.

---

## 6. Configure Dependencies with Winetricks

1. Right-click on the game in Heroic and go to **Settings**.
2. Scroll down and click on **Winetricks**.
3. Search and install the following dependencies:
    - `corefonts` / `allfonts` (Your choice)
    - `vcrun2015`
    - `dotnet48`
4. Wait for the dependencies to install. Be patient—it's not stuck, just taking time.

---

## 7. Adjust Wine Settings

1. Click on **OPEN WINETRICKS GUI**.
2. Select **Select the default wineprefix**.
3. Choose **Change settings**.
4. Enable the following settings:
    - **win11**
    - **renderer=vulkan**
5. Click **OK** and keep pressing **Cancel** until the Winetricks window closes.

---

## 8. Install WinMetadata

1. Unzip the `WinMetadata` folder from the [WinMetadata.zip file](https://archive.org/download/win-metadata/WinMetadata.zip) into `drive_c/windows/system32`.

---

## 9. Complete the Setup

1. Press **Launch** and complete the setup.
2. Once installation is finished:
    - Right-click on the game in Heroic and go to the **Details** tab.
    - Click on the three dots (top-right corner) and select **Edit App/Game**.
    - Change the executable to:  
      `drive_c/Program Files/Affinity/APPNAMEHERE/APPNAMEHERE.exe`
    - Click **Finish** and **Launch** the game.

---

## 10. Performance Settings

To optimize performance and reduce latency, adjust these settings:

- **Other Tab:** Check the **Game Mode** option.

Quote from **darkside99**:  
*"These are the best settings for improving performance and reducing latency."*

![Performance Settings](https://github.com/user-attachments/assets/a274d0d6-538e-4288-9365-73bdf4fa2e16)

---

## 11. Optional: Enable Dark Theme

To enable the dark theme, run [this registry file](https://raw.githubusercontent.com/Twig6943/AffinityOnLinux/refs/heads/main/wine-dark-theme.reg) inside the Wine prefix.