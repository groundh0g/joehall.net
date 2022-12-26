---
layout: post
title:  "My Plans for 2023"
categories: family
author: groundh0g
---

I've been working on my 2016 sprite packing tool (again) recently. [The current version](http://gamedevutils.com/) is web-only, static HTML so that your assets stay on your machine. I don't need to see them, or pay for the server resources to process them. It's cross-browser and cross-platform, so you can work on whatever platform suits your project best. 

<img src='{{ "/assets/images/blog/2016-gamedevutils-sprites.png" | relative_url }}' style="width:512px;" />

## The New Version (Coming Soon)

The new version of the sprite packer still supports a web-based application that's cross-browser and cross-platform, but it also adds desktop applications for Windows, MacOS, and Linux (using ElectronJS), and command-line applications for the same (using NodeJS). The command-line apps allow for build pipelines, and it's something I've wanted to add for some time now.

The original version was written in vanilla Javascript, using Bootstrap and jQuery. The new version is written in Typescript, using ReactJS for the GUI, and is backed by tests. Some new features include:

* attempts to be 100% backwards compatible when opening old projects
* improves performance when packing sprites
* improves logging; adds several new logging levels
* validates selected options, rather than handling conflicts silently
* adds the new Guillotine sprite packing algorithm
* adds Shelf and Skyline sprite packing algorithms
* adds several new sorting algorithms
* infers which heuristic (packer options) to use, based on the selected sort method
* allows for selecting packing heuristic to be used (overrides inferred heuristic)
* adds documentation, supports selecting docs version, defaults to latest
* will likely support rotated sprites (still deciding)

> **NOTE:** This is my first implementation of the Guillotine packing algorithm. I always use JoeRects (my implementation of MaxRects) for my projects, but Guillotine is supposed to be a superior packing method. I'll be kicking the tires on it as you are doing the same. The Shelf and Skyline algorithmms are provided for completeness. I don't use them, but you may have a scenario where they're useful to your purposes.

![Joe's Signature]({{ "/assets/images/signature-joe.png" | relative_url }})
