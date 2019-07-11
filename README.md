## Recovery mode (RCM)

    1. complete switch off (hold power button for 3 sec and choose power down in the menu)
    2. ground pin 10 right joycon rail
    3. press volume up + power (success if seemingly does not turn on)

## Determining if the switch is vulnerable to fusee-gelee

    1. switch in RCM mode
    2. plug switch to pc
    3. run command (A success message should now be displayed on your Switch.)
      sudo python3 ./fusee-launcher.py ./fusee-test.bin