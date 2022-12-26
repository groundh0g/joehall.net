---
layout: post
title:  "Upcoming Changes for GameDevUtils.com, 2023/Q1"
categories: gamedev
author: groundh0g
---

I've been working on my 2016 sprite packing tool (again) recently. The current version is web-only, static HTML so that your assets stay on your machine. I don't need to see them, or pay for the server resources to process them. It's cross-browser and cross-platform, so you can work on whatever platform suits your project best. To see a list of the current features, click the link to [the current version](http://gamedevutils.com/), then click the "Show Features" button, next to the "Sprite Sheets" tool.

<img src='{{ "/assets/images/blog/2016-gamedevutils-sheets.png" | relative_url }}' style="width:512px;" />

One cool feature of the existing tool is that the project file contains everything you need to build your sprite sheet. This includes project options and all project assets. Sharing the project is as easy as handing the (single) file to a teammate. This is a goal shared by all future releases.

The project files support both compressed and uncompressed modes. The uncompressed project file is a standard JSON object - human-readable and easily analyzed or modified when scripting your build pipeline. The compressed project file is a standard ZIP file containing the same JSON when uncompressed.

## The New Version (Coming Soon)

The new version of the sprite packer still supports a web-based application that's cross-browser and cross-platform, but it also adds desktop applications for Windows, MacOS, and Linux ([using ElectronJS](https://www.electronjs.org/)), and command-line applications for the same ([using NodeJS](https://nodejs.org/)). The command-line apps allow for build pipelines, and it's something I've wanted to add for some time now.

## The New Features

The original version was written in vanilla Javascript, using [Bootstrap](https://getbootstrap.com/) and [jQuery](https://jquery.com/). The new version is written in [Typescript](https://www.typescriptlang.org/), [using ReactJS](https://reactjs.org/) for the GUI, and is [backed by tests](https://jestjs.io/). Some new features include:

* attempts to be 100% backwards compatible when opening old projects
* improves performance when packing sprites
* improves logging; adds several new logging levels
* validates selected options, rather than handling conflicts silently
* adds the Guillotine sprite packing algorithm
* adds Shelf and Skyline sprite packing algorithms
* adds several new sorting algorithms
* infers which heuristic (packer options) to use, based on the selected sort method
* allows for selecting packing heuristic to be used (overrides inferred heuristic)
* adds improved / intelligent trimming for animated GIF frames
* adds documentation, supports selecting docs version, defaults to latest
* adds a desktop application for Windows, MacOS, and Linux
* adds a command-line tool for Windows, MacOS, and Linux
* still deciding, but will likely support options that the current version ignores:
  * rotated sprites
  * sprite aliasing (duplicate sprite detection)
  * include @2x sprites

> **NOTE:** This is my first implementation of the Guillotine packing algorithm. I always use JoeRects (my implementation of MaxRects) for my projects, but Guillotine is supposed to be a superior packing method. I'll be kicking the tires on it as you are doing the same. The Shelf and Skyline algorithmms are provided for completeness. I don't use them, but you may have a scenario where they're useful in your workflow.
> 
> **NOTE:** The "Include @2x" option expects the full size sprites, then produces a sheet with @2x sprites, plus a second sheet with sprites at 1/2 their original dimensions.

## The Node Module

The core functionality of these applications is encapsulated as a Node module. It's not yet published, but it will be shortly after the release of the next version of the tool. Packaging the core lib as a Node module allows me to include the same code in the web, desktop, and command-line applications. But you may find it useful too.

## The Documentation

The new release of the [GameDevUtils.com sprite packer](http://gamedevutils.com/webapps/sheets/) will provide detailed documentation. Future releases of the tool will be versioned along with the docs. While the next release will be English-only, I intend to support localization in a future release.

## How You Can Help

If you would like to report an issue or request a new feature, click one of the following links.

* [request a new feature](https://github.com/GameDevUtils/support/issues/new?template=feature_request.md)
* [report a bug in the tool](https://github.com/GameDevUtils/support/issues/new?template=bug_report.md)
* [report an issue with the documentation](https://github.com/GameDevUtils/support/issues/new?template=doc_report.md)

If you're looking to contribute in a more technical capacity, clone the repo, create a branch for your changes, and open a pull request against [this repository](https://github.com/GameDevUtils/gdu-sheets).

Thanks for reading this far!

![Joe's Signature]({{ "/assets/images/signature-joe.png" | relative_url }})
