# Bluetooth Button Assistant

I created this Tasker project to launch Google Assistant or Alexa with a physical button connected to my Samsung phone via bluetooth. It works just by pressing a button, without having to worry about the phone being locked, with the keyguard or unlocked. 

The idea is: all you have to do is press a button and the assistan will pop up and listen to your voice command. Main use for this is for voice commands while driving in the car, to avoid distractions.

**Disclaimer: never use your cell phone while driving. This software is not intended to be used in the car while driving. If you drive a car and wear a phone don't use this software**

## Project need

Several reasons I needed to do this specific development with tasker:
- Yes, you can invoke the assitant saying the hotword "OK Google", or by pressing an specific specific button for that in the stearing wheel if your car is equiped with it, but if you are using Android Auto, assistant functions are very restricted. Specifically you will miss the capability to invoke routines, that stopped to work after some upgrade of AA in 2018 (see: https://www.reddit.com/r/AndroidAuto/comments/b0wiml/routines_from_android_auto/). 
- I use both Google Assistant and Alexa. Alexa is not compatible with Android Auto and you cannot invoke Alexa by saying the hotword on most phones. In recent updates of the app this is possible by requires Alexa app to be in foreground, wich requires the phone to be unlocked.
- Yes, you can remmap a physical button from yor phone (f.i: bixby button) with some of the solutions that are in Google Play store, and make it lauch Google Assistant or Alexa. However you will need the phone to be unlocked to get most commands to work, or it will request you to unlock the phone if it is not. You can configure Smart Lock for the phone to remain unlocked while connected to your cars bluetooth, however if your phone was locked when it connected to bluetooth, Smart Lock will not unlock it (at least with all phones I have tried that). I might use Google Assistant 0 or 1 times on a regular trip. This means 100% of the times I need Smart Lock to have my phone unlocked it will not be of help. Also depending on where you wear you phone it will not be handy to find the physican button.

## Pre-requirements

To run this tasker project you will need:
- A physical bluetooth media button like this: https://www.amazon.com/Satechi-Bluetooth-Multimedia-iPhone-Samsung/dp/B00RM75NL0. You can put it on the stearing wheel or stick with double-sided tape
- Tasker: https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm
- Autoinput: https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput
- Google Assistant app (to be able to lauch the assistant in the phone and not in Android Auto): https://play.google.com/store/apps/details?id=com.google.android.apps.googleassistant
- Alexa app: https://play.google.com/store/apps/details?id=com.amazon.dee.app

## Setup

Installation and configuration:

- Phone should be paired to the bluetooth media button. It is preferible that it is also paired to your car bluetooth. If it is connnected via cable to Android Auto it will also work.
- Always On Display must be set to be on. This is done automtically upon connection to the bluetooth button it will set Allways On Display to allways. After disconnection it will restore previous configuration.
- Autoinput Accessibility service must be on. Even if it is I found that autoinput would not be able to interact with the lock screen (as it accessibillity service had stopped). Murphy's law is unforgiving in these cases, making the chance where it it is not meant to work the one where you need to use it. So after struggling a bit with this I found a workaround by desabling accesibility service and enabling it again upon connection of the bluetooth button. For this workaround to work you will need to give tasker permissions to modify Android Secure settings as described in tasker documentation here: https://tasker.joaoapps.com/userguide/en/help/ah_secure_setting_grant.html
- The %PIN variable in tasker must be filled with the positions of your PIN separated by commas and updated if you change your PIN.
- The %ButtonBTAddress and %ButtonBTName must contain the physical address and name of your bluetooth button.
- There is a reference to a sound "Notifications/OkGoogle.mp3" to make the Google Assistant sond. You might need to record this sound yourself of change it for other notification sound.

## Use

Usage: 
- "Play" btton is remapped to run Google Assistant.
- "Forward" button is remapped to run Alexa.
- "Back" button is remapped to Andoid "Home" button. It can be used to cancel assitant.
- First time you press the button it will connect to bluetoooth. I have mapped this event to run Google Assistant also, so to run Alexa you'll have to press the button a second time.

I hope it works also for you and find or usefull.
