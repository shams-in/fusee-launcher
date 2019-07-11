## Recovery mode (RCM)

    1. complete switch off (hold power button for 3 sec and choose power down in the menu)
    2. ground pin 10 right joycon rail
    ![Pins](https://raw.githubusercontent.com/shams-in/fusee-launcher/master/ground-9%2610.png)
    3. press volume up + power (success if seemingly does not turn on)

## Determining if the switch is vulnerable to fusee-gelee

    1. switch in RCM mode
    2. plug switch to pc
    3. run command
       $ sudo python3 ./fusee-launcher.py ./fusee-test.bin
       (A success message should now be displayed on your Switch.)

It contains _no payloads_. You must download and place the payloads in the "Payloads" directory.

Note: Payload-specific launchers have been removed for now. If demand is there, I will bring them back. I just do not see a point to them with one unified GUI.

Dependencies:

- Python 3
- libusb
- pyusb
- tkinter

1. Install brew via https://brew.sh
2. Install Python 3 and libusb: brew install python libusb
3. Install pyusb: python3 -mpip install pyusb
4. Install tkinter: python3 -mpip install tkinter
   --note-- tkinter is installed on most Python3 installations by default

Usage:

0. Install everything in the above Dependencies area
1. Look at the top of this repository page
1. Click the green button that says "Clone or download"
1. Download ZIP
1. Find where the ZIP downloaded and extract it
1. In the folder that was extracted, place your Fusée payloads in the payloads folder.
1. Enter RCM mode on the Switch (this will not be covered here)
1. While in RCM mode, connect the Switch to a USB port on the computer (using a hub will likely not work!)
1. Doubleclick on macOS launch.command
1. Use the arrow buttons in the window that opens to find your payloads.
1. Press Run.

Troubleshooting
Recieving this error? usb.core.NoBackendError: No backend available
Run the command: brew link --overwrite libusb

If you are recieving issues and wish for help, please open a GitHub issue or let me know on the GBATemp thread.

Include the following information:

MacOS Version String (e.g., 10.14.x). Just giving me the name of the release ("High Sierra") does not help as much.
Mac hardware. Include the model and year, so I know what ports and interfaces you are using.
