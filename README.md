# Enabling Pico VR Motion Trackers in SteamVR Games

This guide provides step-by-step instructions to enable Pico VR motion trackers in SteamVR games by adding necessary files to the Pico Connect application folders.

## Requirements

### **Hardware:**
- **Pico 4** (standard) headset with firmware version 5.11 or later
- **Pico Motion Trackers** (2024 trackers or newer)

### **Software:**
- **Pico Connect** version 10.2.7
- **Pico Tracker App** version 2.0.1

### **Attachments:**
- All necessary JSON configuration files (see [Step 4](#4-add-necessary-json-files-to-the-swift-folder))

## Installation Steps

### 1. Locate the Pico Connect Folder

Navigate to the Pico Connect installation directory:

```
C:\Program Files\PICO Connect\openvr_driver\resources\input\
```

### 2. Replace `pico_tracker_profile.json`

1. **Backup Existing File:**
   - Before making any changes, create a backup of the existing `pico_tracker_profile.json` file.

2. **Replace the File:**
   - Copy the provided `pico_tracker_profile.json` from the attachments.
   - Paste and overwrite the existing `pico_tracker_profile.json` in the Pico Connect folder:
     ```
     C:\Program Files\PICO Connect\openvr_driver\resources\input\pico_tracker_profile.json
     ```

### 3. Create the `swift` Folder (If Missing)

If the `swift` folder does not exist, create it at the following path:

```
C:\Program Files\PICO Connect\openvr_driver\resources\input\swift
```

### 4. Add Necessary JSON Files to the `swift` Folder

1. **Place JSON Files:**
   - Copy all provided JSON files from the Releases page (https://github.com/Elbios/pico-motion-trackers-steamvr-guide/releases) into the `swift` folder:
     ```
     C:\Program Files\PICO Connect\openvr_driver\resources\input\swift\
     ```
   - The required files include (but are not limited to):
     - `legacy_bindings_vive_tracker_handed.json`
     - `pico_tracker_camera_profile.json`
     - `pico_tracker_chest_profile.json`
     - `pico_tracker_keyboard_profile.json`
     - `pico_tracker_left_foot_profile.json`
     - `pico_tracker_left_knee_profile.json`
     - `pico_tracker_left_shoulder_profile.json`
     - `pico_tracker_right_foot_profile.json`
     - `pico_tracker_right_knee_profile.json`
     - `pico_tracker_right_shoulder_profile.json`
     - `pico_tracker_waist_profile.json`
     - `vive_tracker_handed_profile.json`

2. **Verify File Placement:**
   - Ensure all JSON files are correctly placed within the `swift` folder.

### 5. (OPTIONAL - first check if tracking works without it!) Add Binding Files to your game SteamVR Bindings Folder (example for VaM)

1. **Navigate to game SteamVR Bindings Directory:**
   ```
   G:\xr\VaM\Assets\VaMAssets\SteamVR_Bindings\
   ```

2. **Copy Binding Files:**
   - Copy the following binding files from the attachments into the game SteamVR bindings directory:
     - `actions.json`
     - `binding_holographic_hmd.json`
     - `binding_rift.json`
     - `binding_vive.json`
     - `binding_vive_cosmos.json`
     - `binding_vive_pro.json`
     - `binding_vive_tracker_camera.json`
     - `binding_vive_tracker_chest.json`
     - `binding_vive_tracker_keyboard.json`
     - `binding_vive_tracker_left_foot.json`
     - `binding_vive_tracker_left_shoulder.json`
     - `binding_vive_tracker_right_foot.json`
     - `binding_vive_tracker_right_shoulder.json`
     - `binding_vive_tracker_waist.json`
     - `bindings_holographic_controller.json`
     - `bindings_knuckles.json`
     - `bindings_oculus_touch.json`
     - `bindings_vive_controller.json`

## Testing the Setup

### 1. Restart Steam and SteamVR

- **Ensure both Steam and SteamVR are completely closed** before proceeding to avoid conflicts.

### 2. Pair and Calibrate Trackers

1. **Wear Your Pico 4 Headset:**
   - Ensure the headset is properly connected and turned on.

2. **Pair Trackers:**
   - Follow the Pico Tracker App instructions to pair each motion tracker with your headset.

3. **Calibrate Trackers:**
   - Calibrate each tracker as per the Pico Tracker App guidelines to ensure accurate tracking.

### 3. Connect to Pico Connect Server

- **Ensure the Pico Connect server is running** and connected to your headset. This allows communication between your headset and SteamVR.

### 4. Launch SteamVR from Headset

- **Start SteamVR directly from your Pico headset** to ensure it recognizes the connected trackers.

### 5. Verify Tracker Detection

1. **Check Devices in SteamVR:**
   - In SteamVR, verify that trackers appear in the list of devices as green or blue boxes.

2. **Enter SteamVR Environment:**
   - Once inside SteamVR, ensure that trackers are tracking and moving, represented as white square boxes.

### 6. Assign Trackers in SteamVR Overlay

1. **Open SteamVR Overlay:**
   - Press the appropriate button to bring up the SteamVR Overlay while in the SteamVR environment.

2. **Assign Trackers:**
   - Assign trackers to the desired tracking points:
     - **Initial Setup:** Enable **only Waist and Ankles** in the overlay.
     - **Disable all other trackers** for the initial test.

3. **Save Assignments:**
   - After assigning, save the configuration.

### 7. Restart SteamVR After Assignments

- **Restart SteamVR** to apply the tracker assignments and ensure all settings are correctly loaded.


## (VaM-specific) Configuring Tracker Assignments for Full Setup

To utilize all eight trackers, assign them as follows in the SteamVR Tracker Manager:

- **Feet Trackers:** Feet
- **Camera & Keyboard Trackers:** Knees
- **Waist Tracker:** Waist
- **Chest Tracker:** Chest
- **Shoulder Trackers:** Elbows

### (VaM-specific) Aligning Trackers with the Vive 2-Tracker Wizard

1. **Run Vive 2-Tracker Wizard in Embody:**
   - Use the Vive 2-Tracker Wizard in Embody plugin to configure and align the tracker nodes accurately.

2. **Follow the Wizard Instructions:**
   - The wizard will guide you through the alignment process to ensure all trackers are correctly positioned.

---

**Attachments:**

- All necessary JSON files as outlined in [Step 4](#4-add-necessary-json-files-to-the-swift-folder).
