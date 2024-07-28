---
title: "Windows 10 Install To Do List"
permalink: /windows/
---

* TOC 
{:toc}

Windows 10

1. [Install Chrome and Login](https://www.google.com/chrome/)

2. Remove Microsoft Edge and registry update

    cd %PROGRAMFILES(X86)%\Microsoft\Edge\Application\

change dir to version and then installer:

    setup.exe --uninstall --system-level --verbose-logging --force-uninstall

    registry:  HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft

    add key EdgeUpdate 

    add DWORD (32-bit): DoNotUpdateToEdgeWithChromium

3. Install all updates

4. Change UAC, change Taskbar settings (never combine, change icons of taskbar for all, turn off taskbar for multiple displays)

4. System Properties / Advanced / Performance
-or-
    ```SystemPropertiesAdvanced```

5. [Run Bloatbox and community scripts](https://github.com/builtbybel/bloatbox).

6. Obliterate Microstore Store and apps, then bring it back
```
    Get-AppxPackage * | Remove-AppxPackage

    Get-AppxPackage -allusers Microsoft.WindowsStore | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}

    Get-AppxPackage -allusers *windowscalculator* | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}

    Get-AppxPackage -allusers *photos* | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}
```

7. Remove all optional features from Add/Remove

8. Adjust timezone

9. Turn off notifications

10. Turn Off aerosnap

11. Personalize -> Solid Color;  Sidebar: Colors: transparency and accent; Start

## Installs

### Text Editor

* [Visual Studio Code](https://code.visualstudio.com/)
* [Notepad++](https://notepad-plus-plus.org/downloads/)

### Multimedia Edit

* [Gimp](https://www.gimp.org/downloads/)
* [Inkscape](https://inkscape.org/)
* [Sketchup 2017](https://download.cnet.com/SketchUp-Make-2017/3000-6677_4-10257337.html)
* [Audacity](https://www.audacityteam.org/)
* [Shotcut](https://shotcut.org/download/)

### Viewers

* [VLC](https://www.videolan.org/vlc/)

### Gaming

* [Steam](https://store.steampowered.com/about/)


### Office Pattycakes

* [LibreOffice](https://www.libreoffice.org/)
* [GnuCash](https://www.gnucash.org/download.phtml)
* [Xmind 8](https://xmind.app/download/xmind8/)
* [FocusWriter](https://gottcode.org/focuswriter/)


### Site Stuff

* [RubyInstaller](https://rubyinstaller.org/downloads/)
* [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
* [FileZilla](https://filezilla-project.org/download.php?platform=win64)


### Utilities

* [7-zip](https://www.7-zip.org/) / [Peazip](https://peazip.github.io/peazip-64bit.html)

* [Google Drive](https://www.google.com/drive/download/)

* [Logos Bible](https://www.logos.com/get-started)


* [ExactAudioCopy](https://www.exactaudiocopy.de/en/index.php/resources/download/)

* [Scribus](https://www.scribus.net/downloads/)

* [yWriter](http://www.spacejock.com/yWriter7_Download.html)

* [Sumatra](https://www.sumatrapdfreader.org/download-free-pdf-viewer)

* [Trelby](https://www.trelby.org/)

* [HandBrake](https://handbrake.fr/)

* [Google Earth Pro](https://www.google.com/earth/about/versions/#download-pro)

Bluestacks Android emulator

Virtual Box / Extra piece