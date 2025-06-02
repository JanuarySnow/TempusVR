
![](https://raw.githubusercontent.com/JanuarySnow/TempusVR/refs/heads/main/tempusv7galleryimage.webp)


---

**Modlist Support: [Lively's Modding Hub](https://discord.gg/livelymods)**

>[!IMPORTANT]
>Tempus Maledictum VR requires ALL Anniversary Edition DLC for Skyrim, in addition to SkyrimVR, and both to be installed on Steam.

>[!WARNING]
>You must update Skyrim AE to the latest version (1.6.1170) on Steam to install this list.

<header>
    <h1>Contents</h1>
</header>

- [Introduction](#introduction)
  - [System Requirements](#system-requirements)
- [Installation](#installation)
  - [Pre-Installation](#pre-installation)
    - [Installing Microsoft Visual C++ and .NET](#installing-microsoft-visual-c-and-net)
    - [Pagefile and Crash Prevention](#pagefile-and-crash-prevention)
    - [Setting Shader Cache Size (NVIDIA Users Only)](#setting-shader-cache-size-nvidia-users-only)
    - [Steam Setup](#steam-setup)
    - [Changing the Game Language](#changing-the-game-language)
    - [Installing Creation Club Files](#installing-creation-club-files)
  - [Wabbajack Installation](#wabbajack-installation)
    - [Installing Wabbajack](#installing-wabbajack)
    - [Downloading and Installing TempusVR](#downloading-and-installing-TempusVR)
  - [Problems with installation](#problems-with-installation)
- [Post-Installation and Optional Setup](#post-installation-and-optional-setup)
  - [Antivirus Exceptions](#antivirus-exceptions)
  - [Post-Installation Issues and Troubleshooting](#post-installation-issues-and-troubleshooting)
- [Playing the List](#playing-the-list)
  - [Before Launching the Game](#before-launching-the-game)
  - [Actually Playing the Game](#actually-playing-the-game)
- [Updating the modlist](#updating-the-modlist)
- [Removing the Modlist](#removing-the-modlist)
- [Issues](#issues)
- [Credits and Thanks](#credits-and-thanks)

# Introduction

Tempus Maledictum VR is a VR port of Tempus Maledictum by Lively, it is a power fantasy modlist built around Legacy of the Dragonborn, you can read more about the original list here : https://github.com/LivelyDismay/tempus-maledictum


[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

## System Requirements

Based on both internal performance testing and user feedback, the section below outlines my *recommended* system specifications for the list. Please keep in mind that every PC is different, and these recommendations are an estimate based on available data and firsthand reports. Individual performance may vary depending on specific hardware and software configurations, as well as other system optimizations. **Troubleshooting & support for hardware related issues will not be provided.**

>[!WARNING]
>
>- An SSD is **required** to the play the modlist.
>- Only Windows 10 or 11 operating systems are supported. Windows LTSC, special variants, lightened editions or any other modified variant **WILL NOT WORK.** Linux installations also **WILL NOT WORK**.

<Details>
<summary>Clarification on PC Requirements</summary>

I have a 4070ti gpu and a 13700k CPU, I run Virtual Desktop Medium resolution, using SSW at 90 fps, on a Quest 2, and the framerate is steady at those settings
There is an optional mod in the list "VRAMR output" which downscales a lot of the textures, I enable this on my system to reduce stutters, if you have a 4090 or better you may disable it.

</Details>

Downloads Size: ~256 GB  
Install Size: ~367 GB  
Temporary Files: ~40 GB  
**TOTAL:** ~623 GB  

> In case of a a disparity between the listed sizes here and the Wabbajack Gallery, the values here should be more correct as Wabbajack does not properly account for archive compression in the post-installation list.

# Installation

Installing Tempus VR is relatively easy and, if you have Nexus Premium, will be a simple waiting game. If you are updating the modlist, you can safely skip to the [updating section](#updating-the-modlist).

## Pre-Installation

These steps are only required for installing the modlist for the first time. Additionally, many of these steps may be covered in other modlist installs, for new users I suggest reading through here regardless.

### Installing Microsoft Visual C++ and .NET

 1. Install [Visual C++ x64](https://aka.ms/vs/17/release/vc_redist.x64.exe).
 2. Install [.NET Runtime 9.X.X Desktop x64](https://dotnet.microsoft.com/en-us/download/dotnet/9.0).
 3. Install [.NET 6.0 Runtime Desktop x64](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-6.0.30-windows-x64-installer).

>[!WARNING]
>If you already have Visual C++ installed, please make sure you install it again and use the `Repair` option to get the latest version of the redistributables. **Do NOT skip this step or MO2 and the game may fail to launch.**

### Pagefile and Crash Prevention

>[!WARNING]
>Larger Skyrim modlists require a significant amount of memory, running out of memory **will** result in crashes and other potential issues. Due to Tempus VR's size and number of files, this step is **NOT** optional. I do not care how much RAM or VRAM you have, please do this step.

**To set up a Pagefile:**

 1. Press `Win Key + R`
 2. Type `sysdm.cpl ,3` and hit `ENTER`
 3. Navigate to **Performance** and click the box `Settings...`
 4. Click the **Advanced** tab at the top
 5. Under **Virtual Memory** click the box `Change...`
 6. Uncheck `Automatically Manage` if it is checked
 7. Select your disk drive, ideally your fastest solid state drive
 8. Click `Custom Size:`
 9. In the box next to **Initial Size (MB)**, type `40960`
 10. In the box next to **Maximum Size (MB)**, type `40960`
 11. Click `Set`.
 12. Click `OK`.
 13. Click `Apply`.
 14. Click `OK`.
 15. **Restart your PC**.

>[!TIP]
> Your pagefile does not need to be on the same drive as your Wabbajack install or Steam install.

<Details>
<summary>ICYWW: Why do we need a Pagefile?</summary>

Skyrim is a very old game (originally released in 2011) that is built on the [Creation Engine](https://en.wikipedia.org/wiki/Creation_Engine), a engine based off of the [Gamebryo](https://en.wikipedia.org/wiki/Gamebryo) engine that was originally used for Morrowind (released in 2002, *before I was born*).  

Through lots of experience and trial-and-error, we have discovered that increasing the window's pagefile can fix certain types of Skyrim crashes, the two most common examples being `Unhandled native exception occurred at 0x7FF6ADC8DDDA` and `Unhandled native exception occurred at 0x0`.  

But why is this? Skyrim appears to use system memory in very unexpected ways, for example it will frequently dip into the pagefile memory despite there being available RAM. Skyrim heavily favors high speed, low latency RAM (the best you can get as of writing this is 6000MHz and CL30 for DDR5).  

</Details>

### Setting Shader Cache Size (NVIDIA Users Only)

>[!IMPORTANT]
>For NVIDIA users, it is recommended to boost the size of the shader cache. These settings have been shown to improve stability, while it may not be entirely necessary, it is still recommended.

**To do this:**

- Right-click on your desktop and select `NVIDIA Control Panel`
- Navigate and click `Manage 3D Settings`
- Scroll down the **Global Settings** tab until you see **Shader Cache Size**
- Double-click `Driver Default` to the right of **Shader Cache Size** and select `10 GB`
- Click `Apply` in the bottom right hand corner
- Exit out of the application
![](https://raw.githubusercontent.com/iAmMe27/Tahrovin/main/img/ShaderCache.png)

### Steam Setup

>[!WARNING]
>If you have your Steam Library in Program Files, read [this article](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) by LostDragonist. Locations such as Desktop, Documents, Downloads, OneDrive, etc. *will* cause issues with installing and playing the list.

 1. Change Skyrim so it does not [automatically update](https://help.steampowered.com/en/faqs/view/71AB-698D-57EB-178C#disable).
 2. Right click on Skyrim SE and click on properties, untick the `Enable Steam Overlay while in-game.`
 3. Please ensure you follow the steps outlined in the [Installing Creation Club Files](#installing-creation-club-files) section. **DO NOT SKIP THIS STEP OR YOUR INSTALL WILL FAIL.**

### Changing the Game Language

>[!WARNING]
>**The English Steam version of Skyrim VR is the only supported version.**

I understand that this may be frustrating for non-English speaking users or users with the GOG/Bethesda.net versions, but due to the core file differences between the different versions, I am only able to support one game version.

To change your Skyrim VR's language:

 1. Right click on Skyrim VR in Steam
 2. Click `Properties`
 3. Click `Language`
 4. Set the Language to `English`

### Installing Creation Club Files
Please ensure you have launched Skyrim AE from Steam once so you can download all the AE DLC

>[!IMPORTANT]
>
>- **DO NOT** Alt+Tab during this process or it will fail to properly download these files.


## Wabbajack Installation

### Installing Wabbajack

Once you have completed the pre-installation section, follow these steps to install Wabbajack:

1. Create an empty folder named `Wabbajack` on the root of your drive, such as `C:\Wabbajack` for example.
    > - **DO NOT place it in Program Files, User folders (such as Desktop, Documents, Downloads, OneDrive, etc.), in your Skyrim's Steam folder, or in any folders related to the modlist itself (the downloads or install folder).**
    > - The `Wabbajack` folder does not need to be on an SSD, but it makes installing faster. You can set this location to be on an HDD for the sake of saving space.

2. Download the [latest version of Wabbajack](https://github.com/wabbajack-tools/wabbajack/releases/latest/download/Wabbajack.exe) and place the `Wabbajack.exe` file inside the Wabbajack folder you created in Step 1.

3. Double-click the `Wabbajack.exe` file that is now inside your Wabbajack folder to set up the program.

>[!IMPORTANT]
>The list requires Wabbajack version **4.0.0.0 or later**. Installing the modlist on older versions of Wabbajack will result in issues.

### Downloading and Installing TempusVR

>[!CAUTION]
>**A legal copy of Skyrim Anniversary Edition and Skyrim:VR is required.** Pirated copies of the game will cause the installation to fail and even if you manage to somehow get around Wabbajack's built-in piracy prevention measures, SKSE does not work with the cracked exes.  

Downloading and installing TempusVR can take a while depending on your internet connection, PC specs, and if you have Nexus Premium. Without Premium, you will need to manually click the **Slow Download** button for each mod.

To install Tempus VR, complete the following steps.

 1. Open Wabbajack and click `Browse Modlists`
 2. Pick the **Skyrim VR** option from the game filter drop-down box (or use the search bar to find the modlist).
 3. Press the download arrow on the TempusVR UI card and wait for it to download ( it will take a LONG time as the actual file itself is 6GB! )
 4. Set the `Modlist Installation Location` to a folder such as `C:\TempusVR`.
    > - **DO NOT place it in Program Files, User folders (such as Desktop, Documents, Downloads, OneDrive, etc.), or in your Skyrim's Steam folder**
    > - The `Resource Download Location` does not need to be on an SSD, but it makes installing faster. You can set this location to an HDD for the sake of saving space.
 5. Download the files from the [Missing Manual Downloads](#missing-manual-downloads) section and place them in your designated `Resource Download Location` folder.
 6. Press the play arrow to begin.
 7. Turn on your favorite show or a nice long video essay as Wabbajack does its thing. Alternatively read through this readme again.
 8. If the installation is successful, then rejoice and move onto [post installation](#post-installation-and-optional-setup). If the installation is unsuccessful, follow the tips below or the [discord server]([https://discord.gg/4WwqfK5yHg](https://discord.gg/livelymods)) for support.

## Problems with installation

It is possible that you may encounter an error with Wabbajack when installing. Some common issues are listed below.

<Details>
<summary>I'm having trouble downloading Non-Nexus files or specific files!</summary>

Big files can fail to download due to connection issues or website issues. You can either run Wabbajack again or download the missing file manually. If you decide to manually download the file, make sure to place the file(s) inside the folder you set as the `Resource Download Location`.

This issue can also occur with files sources from Google Drive, MEGA, Patreon, and other sites. Missing Manual Downloads are listed [here](#missing-manual-downloads).

</Details>

<Details>
<summary>Wabbajack couldn't find my game folder!</summary>

Either buy the game or re-read the [Pre-Installation](#pre-installation) section.  

</Details>  

<Details>
<summary>Unable to download Skyrim_Default.ini or SkyrimPrefs.ini:</summary>

This error means you failed to follow this Readme. Go back and follow the steps outlines in the [Changing the Game Language](#changing-the-game-language) section

</Details>  

<Details>
<summary>Could not find part of the path "TEMP_BSA_FILES"</summary>

This is typically caused by a problem extracting zip files.  

The quickest solution is as follows:  
 1. Close Wabbajack.
 2. Go to your install folder and locate the `TEMP_BSA_FILES` folder (if it exists).
 3. Delete that folder (if it exists).
 4. Restart Wabbajack.
 5. Restart the modlist installation.  

If the `TEMP_BSA_FILES` folder does not exist, then delete the download file for the mod being referenced before restarting Wabbajack.  

**Note**: Using the retry button will not work as Wabbajack does not understand that there was an issue with extraction and will not retry extraction steps.

</Details>  

<Details>
<summary>My antivirus reports a virus with the program or modlist!</summary>

Windows 10/11 may automatically quarantine a key file which is needed for Mod Organizer. You can fix this by [adding an exclusion for Mod Organizer in windows defender](#antivirus-exceptions).  

</Details>

<Details>
<summary>Sanity check error extracting file:</summary>

Wabbajack will sometimes have issues extracting files if they use special characters. If you encounter this issue in a Wabbajack log, please try the steps down below:

 1. Press `Win Key + R`.
 2. Type `intl.cpl` and hit `ENTER`.
 3. Navigate to *Administrative* and click `Change system locale...`.
 4. Change the *Current system locale:* to `English (United Kingdom)`.
 5. **Uncheck** `Beta: Use Unicode UTF-8 for worldwide language support`
 6. Click `OK`
 7. **Restart your PC** and rerun the Wabbajack installer.

</Details>  

<Details>
<summary>Wabbajack is crashing during the installation!</summary>

If you find yourself struggling to run Wabbajack without it crashing, freezing up, or blue-screening your PC, please try lowering Wabbajack's resource usage with these steps:

 1. Open Wabbajack.
 2. Click the **Settings** button in the bottom left corner of the Wabbajack window.
 3. Under the **Performance** box, lower each number for each category to half of what it is currently set.
 4. Continue Installation.

>[!TIP]
> It is suggested to have a program installed on your PC that can open `.json` files, like [Notepad++](https://notepad-plus-plus.org/) or [Visual Studio Code](https://code.visualstudio.com/)

</Details>  

# Post-Installation and Optional Setup

## Antivirus Exceptions

>[!WARNING]
>Antivirus programs are notorious for false flagging [MO2's Virtual File System](https://stepmodifications.org/wiki/Guide:Mod_Organizer/Advanced), which can and will cause crashes and other problems. Antivirus programs like BitDefender, Norton, and Webroot are especially aggressive, and you will need to fully remove them from your PC in order to actually launch the game through MO2. It is 2024, Windows Defender and being smart online is more than adequate to protect yourself from malicious software.

If you use Windows Defender, it is advised that you set up an exception for the modlist.

<Details>
<summary>Setting up Windows Defender Exceptions:</summary>

 1. Press the Windows Key.
 2. Type "Windows Defender" in the search bar and select "Windows Security".
 3. Click on "Virus & threat protection" in the left pane.
 4. Click the "Manage settings" option under "Virus & threat protection settings".
 5. Scroll down to "Exclusions" and click "Add or remove exclusions".
 6. Windows Defender will prompt you with a run as administrator screen, just hit yes.
 7. Click the "Add an exclusion" button at the top and choose "Folder".
 8. Navigate to your Install folder for the list and click "Select Folder".
 9. **(OPTIONAL)** You can repeat these steps for the other executables:
    - ModOrganizer.exe (`[Path to Modlist]\ModOrganizer.exe`)
    - Nemesis Unlimited Behavior Engine.exe (`[Path to Modlist]\mods\Project New Reign - Nemesis Unlimited Behavior Engine\Nemesis_Engine\Nemesis Unlimited Behavior Engine.exe`)
    - Synthesis.exe (`[Path to Modlist]\tools\Synthesis\Synthesis.exe`)

</Details>  

## Post-Installation Issues and Troubleshooting

<Details>
<summary>Form 43 Error in MO2. / A DLL plugin has failed to load correctly.</summary>

Your installation is corrupt. Rerun Wabbajack and make sure to tick the **Overwrite Installation** box. If the error persists after a reinstall, then delete the `[Path to Modlist]\mods` folder, and rerun Wabbajack again.

</Details>  

<Details>
<summary>Crashes during Gameplay</summary>

I have recently got to level 40 in a playthrough without a *single* crash, I find the list very stable now, but everyones machines are different, if you experience crashing please ensure:

 1. Your crash is reproducible.
 2. You include all relevant crashlogs (if you do not know where to find them then use the `!crashlog` command in chat).
 3. Provide details about the crash (what you were doing, where it took place, if there was an associated quest, etc). Details are necessary in order to quickly diagnose crashes.

and then report it to me in the linked Discord in the #tempusvr-unofficial channel

</Details>

## Actually Playing the Game

 1. Launch the "Play" Executable in MO2. The game may take several minutes to load on your first launch. Please be patient and **DO NOT** click the `Unlock` button on the MO2 prompt.
   >[!CAUTION]
   >**FOR THE LOVE OF AKATOSH, DO NOT CLICK THE UNLOCK BUTTON!**
 2. Select the **New Game** button.
 3. Create your lovely character.
 4. Wait a while for some of the messages to stop appearing in the top left, walk around the room and pick up some stuff if you want.
 6. Pick your class and talk to the little Dragon sitting on a lantern. If no specified start is chosen, then you will have the default start in the Helgen Inn.
 7. Simply open the door next to him and step into the black void gazing at you :)

## Controls

Controls are the base VR essentials are from FUS : <https://github.com/Kvitekvist/FUS/wiki/Controller-bindings-guide>

I use kvites bindings

# Updating the modlist

Versioning for the list will adhere to the following format: `MAJOR.MINOR.PATCH`.

- `MAJOR`: Any release with a number change here will be considered a major update as at least 1 area of the list was massively overhauled. These updates with **NEVER** be save safe.
- `MINOR`: Any release with a number change here will be considered a minor update, these updates will **not** be save safe, unless otherwise specified.
- `PATCH`: Any release with a number change here will be considered a patch, these updates should be save safe and will be used primarily for bugfixes.
- In some rare cases, a fourth number will be used to designate a `HOTFIX`. These will only be utilized in cases where the list is recompiled with no other changes.

Updating is like installing the list. Simply make sure your paths are the same and tick the `overwrite installation` button. Please keep in mind any mods you have added will be deleted when updating. To make sure that Wabbajack does not delete your added mods upon updating, prefix your mods with `[NoDelete]`.

>[!IMPORTANT]
>Saves can be continued across **Save-Safe** updates.

# Removing the Modlist

Simply delete the TempusVR folder. Congratulations, you have uninstalled TempusVR.

# Issues
-some interiors will probably still have some mismatched lighting and floating objects here and there, havnt gone to them all yet

-floating lanterns in falkreath, whatever

-twice now in around 14 hours of my current playthrough, all NPCs will turn invisible, no idea why, a reload fixes it

-my character models' little finger stretches to twice its length temporarily when using the "Prayer" ability, Im not even mad about it tbh


# Credits and Thanks

- Lively for somehow managing to be mostly likeable despite being an asshole, and making Tempus which gave me an idea for a content-rich VR list
- Styxx, idk why theres probably a reason
- Aljo for this readme and various other things hes pretty smart about, like... yeah ive forgotten but theres loads of things
- Jack Daniels

# screenshots:

![Untitle1d](https://github.com/user-attachments/assets/538c2943-7b3f-4847-8306-18448ef212c5)
![Untitle2d](https://github.com/user-attachments/assets/ad0e2342-83a4-4c01-9b8d-e3f8c2ec4c5e)
![ScreenShot3](https://github.com/user-attachments/assets/750a0025-f928-4751-9fd2-a08ed5c7c0bb)
![Untitled](https://github.com/user-attachments/assets/b0f53600-7d99-4725-a378-8b51b687b99b)

