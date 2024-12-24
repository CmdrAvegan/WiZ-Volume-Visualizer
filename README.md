# README for WiZ Volume Audio Visualizer

## Overview

The **WiZ Volume Audio Visualizer Program** is a dynamic application that synchronizes your WiZ smart lights with audio input to create stunning, real-time lighting effects. Featuring a user-friendly GUI and extensive customization options, this program empowers users to control their lights effortlessly.

This README provides a detailed guide to the program's features, setup, and configuration.

---

## Features

### Real-Time Audio Visualization
- Captures audio from the system and translates volume and frequency data into vivid lighting patterns.
- Includes dynamic brightness and smooth color transitions.

### Comprehensive GUI Configuration
- **Audio Settings**:
  - Select audio devices from a dropdown menu.
  - Enable manual input for device indices.
  - Adjust advanced audio processing settings such as sample rate and buffer size.
- **Light Configuration**:
  - Add, remove, or auto-detect WiZ light IP addresses.
  - Set UDP port for communication.
- **Visualization Settings**:
  - Adjust thresholds for beat and drum break detection.
  - Configure intensity and smoothing settings for effects.
- **Brightness Settings**:
  - Set user-defined and minimum brightness levels.
  - Enable or disable dynamic brightness adjustment.
- **Feature Toggles**:
  - Toggle options like color reversal, beat detection, and tempo-based intensity.
- **Color Profiles**:
  - Define vivid, beat, and drum break colors using a color picker.
  - Preview RGB values and adjust dynamically.
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
3. Select your desired audio input device from the dropdown menu or enable manual input to specify the device index.
4. Click **Save** to apply the changes.

### Light Configuration
1. Enter the IP address of your WiZ light(s) in the provided field.
2. For multiple lights, enter each IP address individually or use auto-detect.
3. Use the auto-detect feature to discover lights on your network and add them to the list.
4. Remove any lights you do not wish to be used from the list.
5. Click **Save** to confirm.

### Customizing Visual Effects
1. Adjust brightness, thresholds, and other settings directly in the GUI.
2. Enable or disable features like:
   - Dynamic brightness
   - Interpolation
   - Beat and drum break detection
3. Configure vivid, beat, and drum break color profiles using the color picker.
4. Click **Apply** to save and activate your settings.

---

## Configuring Audio Input

### Option 1: Using Stereo Mix
1. **Enable Stereo Mix**:
   - Right-click the sound icon in your system tray and select **Sounds**.
   - Navigate to the **Recording** tab.
   - Locate **Stereo Mix**, right-click, and select **Enable**.
2. **Set Stereo Mix as the Default Device**:
   - Right-click **Stereo Mix** and choose **Set as Default Device**.
3. Select Stereo Mix in the GUI as your audio device. (Select the Stereo Mix with the correct device index and configurations.)

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
- Play audio and verify that the program detects and visualizes the input. If you notice the program processing audio when no audio is present please adjust your audio volume in Voicemeeter or Stereo Mix audio levels in 'properties'.

---

## Debugging

Enable debug logging in the GUI to save detailed logs to `wiz_vis_debug_log.txt`. These logs can help diagnose issues with audio input, light communication, or configuration.

---

## Dependencies

- [PortAudio](http://www.portaudio.com/): Audio processing.
- [Boost.Asio](https://www.boost.org/doc/libs/release/doc/html/boost_asio.html): UDP communication.
- [nlohmann/json](https://github.com/nlohmann/json): JSON parsing.
- [PyQt5](https://pypi.org/project/PyQt5/): GUI framework.
- [pywizlight](https://pypi.org/project/pywizlight/): WiZ light control.

---

## License

This program is provided "as-is" without warranty. Please ensure compliance with local laws when using this program.

---

If you have questions or need assistance, raise an issue on the GitHub repository.

