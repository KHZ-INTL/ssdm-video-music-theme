

# sddm-video-music theme
This is a SDDM theme based on [@Eayu's](https://github.com/Eayu/sddm-theme-clairvoyance) Clairvoyance theme but also includes code from [@3ximus](https://github.com/3ximus/aerial-sddm-theme) Aerial-sddm-theme. The Clairvoyance theme was modified to have videos play as background and also play music. Music and videos are loaded from a playlist. To avoid reinventing the "wheel" I have used most of the code from the Clairvoyance and aerial-sddm-theme.

## Screenshots and videos
[![Alt text](/screenshots/screenshot_1.png?raw=true)]
[![Alt text](/screenshots/screenshot_2.png?raw=true)]

![preview3](screenshots/1.gif)




## What has changed?
+ User selection is disabled, but you can change that in the Main.qml file:
  + set "ChooseUser" visibility property to true. It is on line 278.
+ The User login image and form is hidden. Press ENTER to make it visible. AFAIT this might be a side effect of hiding the user selection element.

## What is included?
+ Video background: Play videos as background from playlist/s.
  + There are two video playlist files. One for videos that are suitable for day, the other for night. The playlist is selected based on the time. You can fine tune the logic in the Main.qml file at line 355. Thanks to 3ximus.
  + The playlist files are located in the Assets folder in this repo. The file names are "playlist_day.m3u" and "playlist_night.m3u".
  + Videos can be loaded from local hardsik or from the Internet.
  + In regards to populating the video playlist please see 3ximus' [aerial-sddm-theme](https://github.com/3ximus/aerial-sddm-theme) ReadMe.
  
+ Image Background: In case video is not accessible, background image is used. Also used when transitioning between videos.

+ Music: Play music in the background from playlist.
  + The music playlist file "music.m3u" is located in the Assets folder in this repo.
  + Populate the music playlist file by:
    + Write the full path of the music file. One file per line. This can be automated by using shell, see the "Other notes" section of 3ximus' [aerial-sddm-theme](https://github.com/3ximus/aerial-sddm-theme) ReadMe.

+ Time and Date
  + Font changed to Fira Sans
    + Can change font and font size or other properties. See Main.qml line 136.
  + The X and Y coordinates are located in the theme.conf

+ Weather: Not implemented at the moment unfortunately
  + Have the resources to implement it? Send me a email: khz.intl@gmail.com or a pull request.

## Things may be implemented/changed
+ Rounded user icon
+ Move username text below image
+ Weather
+ notifications / Recent notifications

## Dependencies
Since most of the components are used from [@Eayu's Clairvoyance](https://github.com/Eayu/sddm-theme-clairvoyance) and [@3ximus' Aerial-sddm-theme](https://github.com/3ximus/aerial-sddm-theme) you need to have the following installed:
+ sddm
+ qt5
+ ttf-fira-mono

To install them:
+ on Arch linux: 'sudo pacman -S sddm qt5 ttf-fira-mono' 
+ on Debian: 'sudo apt-get install sddm qt5 ttf-fira-mono'

If that is not sufficient to run consider installing:
+ gst-libav 
+ phonon-qt5-gstreamer
+ gst-plugins-good

To install them:
+ on Arch linux: 'sudo pacman -S sddm qt5 ttf-fira-mono' 
+ on Debian: 'sudo apt-get install sddm qt5 ttf-fira-mono'

## Installation<br>
First clone the repository:<br>
```git clone https://github.com/KHZ-INTL/sddm-video-music-theme```<br><br>
Make sure that you have the required dependencies installed.<br>
Then move it to the sddm-themes directory:<br>
```sudo mv sddm-video-music-theme /usr/share/sddm/themes/```<br><br>
Then set the current theme to clairvoyance in sddm.conf:<br>
```sudo vim /etc/sddm.conf```<br>
and set "Current" equal to "sddm-video-music-theme" (no speech marks).

## Credits
Thanks to:
+ [@Eayu's](https://github.com/Eayu/) for his wonderful theme, Clairvoyance. Shamelessly stole his installation instructions, sorry no time to write one my self. 
+ [@3ximus](https://github.com/3ximus/aerial-sddm-theme) for his wonderful theme, Aerial-sddm-theme. Also awesome license. 
+ Apple's Aerial videos.

## License

Theme is licensed under GPL.

