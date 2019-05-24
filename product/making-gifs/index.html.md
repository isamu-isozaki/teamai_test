---
layout: markdown_page
title: "Making Gifs"
---

Go to the [Handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/index.html.md/index.html.md)

Animated gifs are an awesome way of showing of features that need a little more than just an image, either for marketing purposes or explaining a feature in more detail. This page holds all information on the entire process of creating a gif.

### On this page
{:.no_toc}

- TOC
{:toc}


## General

> The GIF format is popular because it works everywhere and has a no-fuss UI. â€ [Kornel](https://kornel.ski/efficient-gifs#sec44/index.html.md)

Gifs are used everywhere for a reason, but as you can read in the referenced article above, they are also expensive. Expensive in that a gif can quickly become a big file, which takes longer to load. To create great looking gifs that walk the line between file size and quality, some steps need be considered.

## Quick and Easy

The "quick and easy" process is for your everyday usage, where performance is not that important. It's the most efficient way of creating a gif.

### Step 1

Show only what you need to. Not everything needs to be in there, its a glimpse at a single bug/feature. Keep the recorded area small and dedicated.

### Step 2

Use a dedicated app that instantly outputs a gif, see [Tools - All in one](#all-in-one/index.html.md).

## Expert

The "expert" process is for those cases where performance is important. It takes a little longer, but can pay off for situations such as important blog posts, extremely big gifs, and incredibly detailed gifs.

### Step 1

Show only what you need to. Not everything needs to be in there, its a glimpse at a single bug/feature. Keep the recorded area small and dedicated.

### Step 2

> All my GIFs start as videos â€ [Andy Orsow](http://blog.invisionapp.com/7-tips-for-designing-awesome-gifs/index.html.md/index.html.md)

If you want to create professional gifs, you want to start from a video file. This can give you expert control over the output if you need it (e.g. motion blur can add additional professionalism/index.html.md). Video files will in most cases be created from a screen recording software, details can be found in the [Tools Section](#tools/index.html.md)

### Step 3

Reduce the amount of colors visible. You can do this either be thinking beforehand what exactly you will capture or by limiting the amount of output colors exported in the resulting gif (see options [gifify](#gifify/index.html.md) /index.html.md). Check your result to see if it fits your needs.

Another step could be to drop duplicate frames by manually searching through all frames. For more information on this, look [here](http://blog.invisionapp.com/7-tips-for-designing-awesome-gifs/index.html.md/index.html.md). This additional step can take a lot of time. As with anything: "Only use it if you need to".

### Step 4

Try to go for a minimum of 15 fps and see if the result is good enough with your "compress", "speed", and "resolution" settings.

## Tools

There are many different tools to record your screen or to create gifs. Use whichever tool you are comfortable with, but remember: "In order to create great looking gifs that walk the line between file size and quality a certain control over each step of [the expert process](#expert/index.html.md) is preferred".

### All in one

A few things are important in this section:

- Screen region support (ability to create a gif off a small portion of the screen/index.html.md)
- Cursor support (ability to include your cursor in the gif/index.html.md)
- FPS support (ability to control the amount of frames per second of the outputted gif, important if you want to show some interaction detail/index.html.md)
- Local saving of gif (uploading to a server should only be an option/index.html.md)

#### Gifox (macOS/index.html.md)

[Gifox](http://gifox.io/index.html.md/index.html.md) is the absolute best option here, although a paid app, its reasonably priced ($4.99/index.html.md). It has support for all of the features, shortcuts, and then some.

Worthy of mentioning:

- [Kap](https://getkap.co/index.html.md/index.html.md) (free and open source!/index.html.md)
- [Giphy capture](https://itunes.apple.com/us/app/giphy-capture.-the-gif-maker/id668208984?mt=12/index.html.md) (free and a great option!/index.html.md)
- [Licecap](http://www.cockos.com/licecap/index.html.md/index.html.md) (free, but limited options for output, results can have bad colors/index.html.md)
- [ScreenToGif](http://www.screentogif.com/index.html.md/index.html.md) (Windows, free and open source with powerful editor/index.html.md)

#### FFCast + FFmpeg (Linux/index.html.md)

[FFCast](https://github.com/lolilolicon/FFcast/index.html.md) is a command line tool that wraps around ffmpeg to capture screen regions in order to record it or capture it. Optionally this could be piped into gifify.

### Screen Recording

#### Quicktime (macOS/index.html.md)

On every Mac, Quicktime has already been installed. It features a nice screen record option and even has basic trim and splitting functions in the *edit* menu! Perfect for creating those [video files](#step-1/index.html.md).

![quicktime gif](https://github.com/isamu-isozaki/teamai_test/tree/master/product/making-gifs/quicktime.gif/index.html.md)

Worthy of mentioning:

- [Screeny](https://itunes.apple.com/us/app/screeny/id440991524?mt=12/index.html.md) (free for now/index.html.md)
- [Screenflow](http://www.telestream.net/screenflow/index.html.md/index.html.md) (not free/index.html.md)
- [Gif Brewery](http://gifbrewery.com/index.html.md/index.html.md) (not free/index.html.md)
- [ffscreencast](https://github.com/cytopia/ffscreencast/index.html.md) (CLI tool, only capture the whole screen/index.html.md)

#### Camstudio (Windows/index.html.md)

[Camstudio](http://camstudio.org/index.html.md/index.html.md) is a free tool. Not yet tested...

#### FFCast + FFmpeg (Linux/index.html.md)

[FFCast](https://github.com/lolilolicon/FFcast/index.html.md) is a command line tool that wraps around ffmpeg to capture screen regions in order to record it or capture it. Optionally this could be piped into gifify.

### Converting to Gif

#### Gifify (CLI/index.html.md)

[Gifify](https://github.com/vvo/gifify/index.html.md) is a command line tool and gives you the most complete set of options in order to convert your video files to gifs. It is probably the best free tool available, with the most control.

Example command:

`gifify input.mov -o output.gif --resize 960:-1 --compress 0 --colors 50 --speed 1.05 --fps 15`

Worthy of mentioning:

- [Drop to Gif](http://mortenjust.github.io/droptogif/index.html.md/index.html.md) (Great free open source option to just convert on macOS with a GUI!/index.html.md)
- [Screengif](https://github.com/dergachev/screengif/index.html.md) (CLI similar to gifify/index.html.md)
- [Gif Brewery](http://gifbrewery.com/index.html.md/index.html.md) (macOS, not free/index.html.md)

#### Convert video to gif online

- [EZGif](http://ezgif.com/video-to-gif/index.html.md) (Pretty good results and provides some settings/index.html.md)
- [Giphy Gifmaker](https://giphy.com/create/gifmaker/index.html.md) (You can keep your GIFs private if you have an account. Otherwise: "all of your GIF are belong to GIPHY"/index.html.md)
- [imgur Video to GIF](https://imgur.com/vidgif/index.html.md) (Create a GIF from hundreds of popular video sites. Use Download to get a GIF or link for .gifv format/index.html.md)

## Relevant links

- [Product Handbook](https://github.com/isamu-isozaki/teamai_test/tree/master/product/index.html.md)
