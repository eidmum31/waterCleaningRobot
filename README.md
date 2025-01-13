# Water Cleaning Robot
Water Cleaning Robot "Protentus" is a robot that floats on the water of rivers, loads the rubbish onto its body and return to the shore to get the rubbish collected.
It can controlled by an Flysky RC which communicates by PPM communication protocol or through nRF RC and nRF communication protocol.

## Project details
The robot body consists of 2 dc motors that control the loader bucket, 2 water pumps to control the robot motion and speed in water.
It also has a flashlight and an ESP-32 WI-FI camera.

## Code breakdown
The logic starts by checking whether the FlySky reciever is connecter or the nRF module is connected, upon which the communication control is chosen.
For PPM communication, pin change interrupt is used in order to count the high time for each channel from the 6 channels, which is then represents data.
For nRF communication, the nRF module is configured to recieve data from the transmitting nRF.
Then, the dc motors and the pumps are controlled accordingly.
