# My Tasker Projects

This repo is a compilation of tasker projects I have built for different personal needs in my day to day. More info about tasker "ecosystem": https://tasker.joaoapps.com/. More info about each project in each folder:

## Find My Phone

Make your phone ring and turn on flashlight by saying a command to your Google Home or Alexa assistant. It integrates with tasker via IFTTT -> Join --> Tasker. Besides Taker, you will need Join setup in your phone. You'll also need an IFTTT account and setup a simple applet that invokes Join after your vouce command, via a Join webhook.

More info: 

- IFTTT: https://ifttt.com/
- Join: https://joaoapps.com/join/
- Integrate IFTTT and Join to lauch Tasker commands: https://joaoapps.com/join/ifttt/

## Ignore Anoying WhatsApp Messages

Intercept certain incomming WhatsApp notifications (that can be from certain contact even if he/she writes in a group) and inmediatly marks them as read, deleting the notification and making message show as already read, efectively allowing you to ignore that messages. You'll never see pending messages in WhatsApp or in your notifications from that person.

## OK Google to Alexa bridge (for Android Auto)

Invoke Alexa on your phone through "OK Google" voice commands. Anytime you say: "OK Google Alexa do something" it will launch Alexa app (through Google Home --> IFTTH -->  Join --> Tasker integration explained above) and repeat the same command "do something" to Alexa, so it can be processed. It unlocks the device if needed before running Alexa app. Can be used to invoke Alexa from Android Auto.

## Read WhatsApp Voice Notes (for Android Auto)

Ask Google Assistant or Alexa to read your WhatsApp voice notes without unlocking the phone. You can ask it to read last voice note and also to move to previous/next voice note. Can be used to listen incoming voice notes in Android Auto (for some reason it does not rean inconing messages that have a voice note, only tells you that a message is a voice note).

## Car Multimedia Tasker
  
Android/Tasker project to setup car multimedia when phone is connected. Effectively blocking auto play that most car multimedia system do by default, so you can decide when the music plays.

## Bluetooth Button Assistant

I created this Tasker project to launch Google Assistant or Alexa with a physical button connected to my Samsung phone via bluetooth. It works just by pressing a button, without having to worry about the phone being locked, with the keyguard or unlocked. 

## Utils

Compilation of different generic routines needed across projects. You might need to import this project to resolve dependencies from the projects above.
