# Candle-manager
A web-based tool for creating and uploading Arduino code. Designed to be beginner friendly.

![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/dashboard.png)

Create new code from built-in templates. The templates are just normal Arduino code themselves which are placed in the 'source' directory.
![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/create_new.png)

The template code's settings are translated into an easy to use interface. After changing settings a new version of the code is generated. This way the user never has to edit code.
![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/code_ux_generation.png)

The new code can then be upload via the upload wizard:
![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/upload_wizard.png)

![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/upload_wizard2.png)

![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/upload_wizard3.png)

![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/uploading_worked.png)

After the code is uploaded to the attached Arduino you can listen to the serial output of the Arduino:
![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/device_doctor.png)

![alt text](https://raw.githubusercontent.com/createcandle/Candle-manager/master/screenshots/editing_code.png)


# What is this designed for?
It's designed to be used with a Rasperry Pi. Users can program Arduino's by connecting them to the Raspberry Pi and then using this tool. More precisely, it's intended to be used inconjuction with MySensors, the Mozilla Gateway and MySController-rs as part of a later to be revealed privacy friendly smart home demonstrator.

https://github.com/mysensors
https://github.com/mozilla-iot/gateway
https://github.com/tsathishkumar/MySController-rs


# What is this useful for?

- Workshops. When users don't have to install Arduino IDE this saves time and hassle.
- Situations where you want people to create Arduino-based devices without immediately confronting them with code. You could easily completely hide the code and other complexity (such as debug output) from the user.
- Smart home solutions, especially ones that use the MySensors framework.


# Future plans, ideas and thoughts
- The Mozilla Gateway is looking for a way for third party creations like this to be integrated. See: https://github.com/mozilla-iot/gateway/issues/1505
- Could be integrated further with MySController-rs. The Candle Manager already grabs data on wirelessly connected devices from it. MySController-rs can be found here: https://github.com/tsathishkumar/MySController-rs


# Installation

- ssh into your raspberry pi
- enter these commands:

```
git clone https://github.com/createcandle/Candle-manager.git
chmod +x ./Candle-manager/start.sh
./Candle-manager/start.sh
```

That should create a new folder "Candle-manager". inside it you will find a folder called "source". This is were you can place Arduino sketches that you want to use as 'templates' for new bits of code. The example that's already present will show you how you can optimise your sketches so that they support creating a visual settings interface, as well as auto-installing of libraries.

Optional:
- Tip: Install this on the Mozilla Gateway.
- Tip: Install MySController-rs as well.


# Other things
- It was inspired by https://github.com/rakeshpai/mysensors-network-manager
- Version 0.3.3 of the Arduino CLI is packaged in. It works for Arm based devices such as the Raspberry Pi. You can check if a new version of the CLI is available. If you use a another platform like Windows that uses Intel chips you will have to download the version of the CLI for that manually.
