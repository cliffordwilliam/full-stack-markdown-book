---
layout: post
title:  "Text Editors"
---

Lesson contents:

* TOC
{:toc}

## Introduction

This is what developer use to write code, it has features that saves time in comparison when writing it on notepad.

## Why can't I use Microsoft Word?

Because that is a rich text editor, those are used to write paper and their files have info not only on text but also visuals like colors, position and graphics data like images. Text editors like VSCode and Sublime saves only text data, which allows interpreter to read and turn it into machine code that your computer can read.

## Code editors

Think of it like a notepad but with features that helps you avoid typos and color codes some key words to make reading faster. There are many text editors but here we recommend Visual Studio Code to start with. This is free, many add-on, great Git integration and easy to use, works the same on any OS.

## VSCode Installation WSL2

### Step 1: Install VSCode

- Follow the instructions for [Visual Studio Code on Windows](https://code.visualstudio.com/docs/setup/windows) to install VSCode.

### Step 2: Delete the installer file

- Open **downloads** directory.
- Delete **VSCodeUserSetup-{version}.exe**.

### Step 3: Install WSL Extension

- Open Visual Studio Code.
- Go to extensions tab.
- Install [WSL extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl).

### Step 4: Ensure that WSL2 can correctly open VSCode

- Open new WSL2 terminal.
- Run this command to open a new VSCode window.
  ```
  code
  ```
- When VSCode opens it should notify you that its opening in WSL2.

## Outside sources

Sections from here on out are from outside sources.

## VSCode Tutorial for Beginners

TODO

## Additional resources

TODO
