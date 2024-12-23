# WiZ Light Audio Volume Visualizer

## Overview

The **WiZ Light Audio Volume Visualizer** is a dynamic application that synchronizes your WiZ smart lights with audio input to create stunning, real-time lighting effects. Featuring a user-friendly GUI and extensive customization options, this program empowers users to control their lights effortlessly.

This README provides a detailed guide to the program's features, setup, and configuration.

---

## Features

### Real-Time Audio Visualization
- Captures audio from the system and translates volume and frequency data into vivid lighting patterns.
- Includes dynamic brightness and smooth color transitions.

### Comprehensive GUI Configuration
- Set your audio device and light IP address directly from the GUI.
- Modify all program variables and options, including:
  - Brightness settings
  - Visualization thresholds
  - Detection toggles (e.g., beat and drum break detection)
  - Color profiles
- Automatically saves configurations to `volume_config.json`, eliminating the need for manual file edits.

### Advanced Audio Effects
- **Drum Break Detection**: Recognizes sudden audio spikes to trigger visual bursts.
- **Beat Detection**: Synchronizes rhythmic patterns with detected beats.

### Networking Support
- Sends UDP commands to one or multiple WiZ lights seamlessly.

### Debugging and Logging
- Optional debug logging to identify and resolve issues.

---

## Installation

1. Run the installer provided to set up the program.
2. Launch the application using the installed shortcut or executable.

---

## Using the GUI

### Audio Device Setup
1. Open the application.
2. Navigate to the audio settings in the GUI.
3. Select your desired audio input device from the dropdown menu.
4. Click **Save Configuration** to apply the changes.

### Light Configuration
1. Enter the IP address of your WiZ light(s) in the provided field or use the Auto-detect IP.
2. For multiple lights, enter one IP Address then click ADD or use Auto-detect.
3. Remove any light's IP from the list you do not wish to use.
4. Click **Save Configuration** to confirm.

### Customizing Visual Effects
1. Adjust brightness, thresholds, and other settings directly in the GUI.
2. Enable or disable features like:
   - Dynamic brightness
   - Interpolation
   - Beat and drum break detection
3. Configure vivid, beat, and drum break color profiles.
4. Click **Save Configuration** to save and activate your settings. Settings are automatically saved when starting the visualizer.

---

## Configuring Audio Input

### Option 1: Using Stereo Mix
1. **Enable Stereo Mix**:
   - Right-click the sound icon in your system tray and select **Sounds**.
   - Navigate to the **Recording** tab.
   - Locate **Stereo Mix**, right-click, and select **Enable**.
2. **Set Stereo Mix as the Default Device**:
   - Right-click **Stereo Mix** and choose **Set as Default Device**.
3. Select Stereo Mix in the GUI as your audio device.

### Option 2: Using VB Audio Cable and Voicemeeter
If Stereo Mix is unavailable, follow these steps:

#### Step 1: Install VB Audio Cable
1. Download VB Audio Cable from [VB Audio Cable](https://vb-audio.com/Cable/).
2. Run the installer and follow the prompts.

#### Step 2: Install Voicemeeter
1. Download Voicemeeter from [Voicemeeter](https://vb-audio.com/Voicemeeter/).
2. Run the installer and restart your computer.

#### Step 3: Configure VB Audio Cable and Voicemeeter
1. **Set VB Cable as Default Output**:
   - Go to **Sound Settings** and set **VB-Cable Input** as the default output device.
2. **Route Audio Through Voicemeeter**:
   - Open Voicemeeter and configure:
     - **Hardware Input 1**: Your microphone or preferred input device.
     - **Virtual Input**: System audio.
     - **Hardware Out (A1)**: Your speakers or headphones.
3. **Select Voicemeeter as Input**:
   - In the GUI, choose **Voicemeeter Output** as the audio device.

#### Step 4: Test the Setup
- Play audio and verify that the program detects and visualizes the input.

---

## Debugging

Enable debug logging in the GUI to save detailed logs to `wiz_vis_debug_log.txt`. These logs can help diagnose issues with audio input, light communication, or configuration.

---

## Dependencies

- [PortAudio](http://www.portaudio.com/): Audio processing.
- [Boost.Asio](https://www.boost.org/doc/libs/release/doc/html/boost_asio.html): UDP communication.
- [nlohmann/json](https://github.com/nlohmann/json): JSON parsing.

---

## License

This program is provided "as-is" without warranty. Please ensure compliance with local laws when using this program.

---

If you have questions or need assistance, raise an issue on the GitHub repository.

