# CarMultimediaTasker
Android/Tasker project to setup car multimedia when phone is connected. Effectively blocking auto play that most car multimedia system do by deffault, so you can decide when the music plays.

Annoyed by your phone multimedia being automatically launched every time you get into your car and have bluetooth connected?

I built this project with different parts of code taken from several other projects and messages in forums cause I couldn't find anything that effectively solves that problem 100% of the times.

It has been tested with Toyota Touch 2 multimedia system and a Samsung Glaxy S10e but should work with others.

This project contains Tasker profiles and tasks needed. You will have to download and setup tasker (https://tasker.joaoapps.com/) and edit the profile to set the name and/or address of your bluetooth equipment.

References: 
https://www.reddit.com/r/tasker/comments/5d3ckl/playpause_currently_running_media/ (only method that I could test that actually works to pause multimedia all players including Alexa and Spotify).

https://www.xda-developers.com/how-to-disable-bluetooth-automatic-playback-on-any-android-phone/ (other method that did not work for me).

The contrubution of this project to the above method is to solve the race condition problem that happen between the moment the bluetooth connection and the multimedia auto-play events are fired, that in my case caused any other methods to solve this problem to fail.
