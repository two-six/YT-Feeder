- [IMPORTANT](#org24a3efb)
- [Introduction](#orgd80fe05)
- [Usage](#orgf01b8d1)
  - [Worth noting](#orgb34af34)
- [Configuration](#org225a399)
- [Requirements](#org20d8c62)
- [TODO](#orgcc8d23e)


<a id="org24a3efb"></a>

# IMPORTANT

1.  **There was an important change to the config file syntax, check it before filling an issue. It was required to make sure some edge cases works and it makes it easier to manage configuration file. There probably won&rsquo;t be another syntax change, this one can be considered final**
2.  There is an issue with bots &ldquo;advertising&rdquo; this project to random people on Discord, asking for stars and offering free Discord Nitro in exchange. I don&rsquo;t know who these people are and why they are doing that, but if you expect any kind of reward for giving a star my project, please don&rsquo;t do it. Having said that, I hope you enjoy using my script 🙂


<a id="orgd80fe05"></a>

# Introduction

**[YT-Feeder Example Video](https://youtu.be/7dMLBVUZDJs)**

YT-Feeder is a Rofi-Based RSS Reader made specifically for YouTube video platform. It&rsquo;s written purely in bash and allows user to watch or download new videos.


<a id="orgf01b8d1"></a>

# Usage

While in the project folder:

```bash
chmod +x YT-Feeder
```

Then to actually run the script:

```bash
rofi -show YT-Feeder -modi "YT-Feeder:Absolute/Path/To/YT-Feeder"
```

I highly suggest binding the above command to your keyboard shortcut of choice. After launch you can select your favorite channel from the list, then select video and then you have a choice to:

-   watch(best) -> watch it in the best quality
-   watch(worst) -> watch it in the worst quality
-   play in the background -> play audio from video in the background
-   download -> download video
-   download audio -> download audio from video
-   command -> use your custom command on video&rsquo;s link

There&rsquo;s also an option to refresh the RSS feeds at the top of the list and there might be an option to stop currently playing audio in the background(only after selecting &ldquo;play in the background&rdquo;).


<a id="orgb34af34"></a>

## Worth noting

The default directory for downloaded videos is ~/Videos/ and the default directory for downloaded audio is ~/Music/.


<a id="org225a399"></a>

# Configuration

Change ~/.config/yt-feeder/config file to configure this script. If it doesn&rsquo;t exist, create it. The general syntax for this file is:

```
// Some comment
rss link or channel's ID
rss link or channel's ID
rss link or channel's ID
DOWNLOAD|~/Videos/folder_for_yt_videos
COMMAND|my_custom_command
DOWNLOAD_AUDIO|~/Music/folder_for_yt_audio
```

Comments must be placed on separate lines, every line starting with &ldquo;//&rdquo; will be ignored by the script

-   `DOWNLOAD` specifies the custom directory where you wish to download your videos.
-   `COMMAND` specifies your custom command to use on youtube links.
-   `DOWNLOAD_AUDIO` specifies the custom directory where you wish to download your audio.


<a id="org20d8c62"></a>

# Requirements

Currently only requirements are:

-   mpv
-   youtube-dl
-   rofi


<a id="orgcc8d23e"></a>

# TODO

-   [X] Add information about the number of new videos
-   [X] Auto-detect Channel&rsquo;s name from RSS Feed
-   [X] Clean bash code
-   [X] Add option to change the default directory of downloaded videos
-   [X] Add option to play video in the background
-   [X] Add an ability to just use channel&rsquo;s ID in the config file
-   [X] Add option to use a custom script on selected video
