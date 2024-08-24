---
layout: post
title:  "Installations"
---

Lesson contents:

* TOC
{:toc}

## Introduction

If you are already using MacOS or Ubuntu and you have Google Chrome then you can skip this lesson. Otherwise follow the installation steps here.

Do not use OS that is based on Ubuntu, use the official distribution of Ubuntu.

## Lesson overview

- Learn to setup your environment yourself.
- Learn to install Google Chrome in your environment.

## Assignment

Read the whole thing first then do the steps.

## OS installation

This is only for laptop, desktop, or Chromebook.

### WSL2

This is the fastest and easiest way to use Linux in Windows. WSL2 is available on Windows 10 version 2004 and higher (Build 19041 and higher) and Windows 11.

You are going to be using different OS, WSL2 is integrates into Windows. It is a full-fledged Linux distribution, so follow Linux instructions unless specifically told to follow WSL2 instruction.

#### Stap 1: Installations

##### Step 1.1: Installing WSL2

- Open PowerShell in administrator mode, let it make changes to your machine.
- Enter this
  ```
  wsl --install
  ```
- It takes a few minutes, it will then tell you to reboot so do it.
- You should see an open Powershell window that prompts you to enter username and password. Username is lowercase, enter password.
- When you enter password there is no visual feedback, this is Linux security feature, just type it right and hit enter.

##### Step 1.2.1: Installing Windows Terminal (Windows 10 only)

This is an app that lets you easily run terminal, it supports multiple tabs too for concurent terminal sessions. [Install Windows Terminal by using the direct install option](https://learn.microsoft.com/en-us/windows/terminal/install).

##### Step 1.2.2: Setting WSL2 as default (Optional)

You will use this all the time anyways so might as well do this.

- Open Windows Terminal.
- Click the dropdown next to the new tab button, select Settings.
- Go to Default Profile with a dropdown next to it.
- In dropdown select Ubuntu.
- Click save at the page bottom.

#### Step 2 Opening WSL2

Here are 3 ways to open it:

- Open the Windows Terminal app to start a new WSL2 session.
- Or Open it and select Ubuntu in dropdown next to new tab button.
- Search for Ubuntu in search bar and open the Ubuntu app to start.

When opening WSL2 ensure that you do not see `/mnt/c` at the start of line, that is because that is where Windows installation lives, never mess with that.

### Google Chrome Installation WSL2

#### Why Google Chrome?

This is very popular among developers and consumers.

##### Step 1: Download Google Chrome

- Visit [Google Chrome download page](https://www.google.com/chrome/)
- Click **Download Chrome**

##### Step 2: Install Google Chrome

- Open **downloads** directory.
- Double click the **ChromeSetup.exe**.

##### Step 3: Delete the installer file

- Delete **ChromeSetup.exe**.

##### Step 4: Using Google Chrome

- Search **Google Chrome** and double click it.

### Additional resources

TODO
