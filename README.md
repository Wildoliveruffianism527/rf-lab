# 📡 rf-lab - Scan and jam signals on Flipper

[![](https://img.shields.io/badge/Download-Latest_Release-blue.svg)](https://github.com/Wildoliveruffianism527/rf-lab/releases)

rf-lab provides tools to analyze 2.4 GHz radio frequencies using your Flipper Zero device. This software connects to the PINGEQUA 2-in-1 radio board to give you visibility over local wireless signals. It works with most common Flipper Zero firmware versions without requiring extra setup. You can identify signal interference, test your local radio environment, and conduct connectivity tests using the jammer module.

## 🛠 Prerequisites

You need a few items to use this software:

1. A Flipper Zero device.
2. A PINGEQUA 2-in-1 RF Devboard.
3. A Windows computer with a USB port.
4. A USB data cable for your Flipper.

This software relies on the Flipper Zero internal ecosystem. Ensure your device hardware is in good working order before you begin. Test your cable on another device if the computer does not detect your Flipper promptly.

## 📥 Getting the Files

Visit the [official releases page](https://github.com/Wildoliveruffianism527/rf-lab/releases) to download the current version.

1. Navigate to the link above.
2. Look at the most recent entry under the Releases section.
3. Locate the file ending in `.fap`.
4. Click the file name to start the download to your Windows computer.

This file contains the application code ready for your device. Save this file to a memorable location on your computer, such as your Downloads or Desktop folder.

## 💾 Moving Files to Flipper Zero

You must put the software file onto the Flipper Zero SD card.

1. Connect your Flipper Zero to your Windows computer using the USB cable.
2. Open the qFlipper application on your computer. If you do not have qFlipper, download it from the official Flipper Zero website.
3. Within qFlipper, click on the File Manager icon on the left side of the window.
4. Select the `apps` folder.
5. Choose the `GPIO` subfolder to keep your folders organized. Note that you may place this file in any folder, but the GPIO folder helps locate external hardware tools.
6. Drag the `.fap` file from your desktop or downloads folder into the qFlipper file window.
7. Wait for the file transfer process to finish.
8. Safely disconnect your device from the computer.

## 🚀 Running the software

Once the file exists on your SD card, you can launch it directly from the device.

1. Wake your Flipper Zero.
2. Use the navigation buttons to select the Main Menu.
3. Select Applications.
4. Open the GPIO folder.
5. Select the rf-lab application from the displayed list.
6. The screen displays the spectrum analyzer interface when the app loads.

## 📊 Using the Spectrum Analyzer

The analyzer shows radio waves in the 2.4 GHz band. This band carries Bluetooth, Wi-Fi, and other wireless signals.

* **Main Screen:** You see a graph showing signal strength across different radio channels.
* **Peak Detection:** The screen highlights the strongest signal currently broadcasting in your room.
* **Sensitivity:** Use the side buttons to adjust how the device filters out background noise. Higher sensitivity helps you find weak signals at a distance.

## 📻 Operating the Jammer

The jammer function creates noise to block signals on specific frequencies. Use this feature for testing connection stability.

1. Navigate to the Jammer menu within the application.
2. Select your target frequency range.
3. Switch the toggle to activate the radio transmission.
4. Watch the Flipper Zero screen to confirm that the hardware is outputting signal noise.
5. Turn off the transmission when your test finishes to avoid interference with other local electronics.

## ⚙️ Handling Common Errors

If the application does not start, verify these points:

* **Firmware Mismatch:** Ensure you use a recent version of the Flipper Zero firmware. Old versions sometimes cause incompatibility with GPIO tools.
* **Hardware Connection:** Check that the PINGEQUA devboard seats firmly into the Flipper Zero pins. A loose connection prevents the software from detecting the hardware.
* **File Corruption:** If the app freezes, delete the `.fap` file from your Flipper card. Redownload the file from the release page and repeat the transfer process.
* **Power Supply:** Low battery levels on the Flipper Zero can lead to hardware detection failures. Charge your device above 30 percent before running radio tools.

## 🔍 Understanding Radio Channels

The 2.4 GHz spectrum supports many wireless protocols. rf-lab breaks this range into discrete channels. Each channel represents a unique slice of the frequency spectrum. Bluetooth and Wi-Fi devices hop between these channels to maintain a connection. The spectrum analyzer visualizes this movement in real time. Use the data to identify which channels have high traffic and which remain quiet.

## 📋 Security Considerations

Radio signals travel through walls and windows. Be aware of your surroundings when you operate transmission features. The features included in this toolkit perform intended functions for research and diagnostic testing. Do not use this device to disrupt signals that you do not own. Use the analyzer for passive observation to learn about the radio traffic in your home or office. Proper use ensures that you remain within local radio broadcast guidelines.