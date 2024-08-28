---
title: "Android Notes"
permalink: /android/
---

## Setup

1. Factory Wipe
2. Opt out of initial legalse and avoid wifi setup
3. Click crazy on build number and to reach developer mode
4. Developer options -> USB Debugging

## ADB

Plug in and run

```
adb devices

```
click back on phone to allow for USB Debugging

```
adb shell
```
To Show everything installed:

```
pm list packages
```

## Verizon Yard Trash, Galaxy Store, Galaxy Theme Store, tips, EMAIL, Chrome, Gmail, "Google", Game LAUNCHER, AR zone, Samsung browser;  Samsung password pay suite; google services and MUCH, MUCH MORE!

```
pm uninstall -k --user 0 com.vcast.mediamanager
pm uninstall -k --user 0 com.verizon.llkagent
pm uninstall -k --user 0 com.verizon.mips.services
pm uninstall -k --user 0 com.verizon.obdm
pm uninstall -k --user 0 com.verizon.obdm_permissions
pm uninstall -k --user 0 com.verizon.onetalk.dialer
pm uninstall -k --user 0 com.vzw.apnlib
pm uninstall -k --user 0 com.vzw.ecid
pm uninstall -k --user 0 com.vzw.hss.myverizon
pm uninstall -k --user 0 com.securityandprivacy.android.verizon.vms
pm uninstall -k --user 0 com.sec.android.app.samsungapps
pm uninstall -k --user 0 com.samsung.android.themestore
pm uninstall -k --user 0 com.samsung.android.app.tips
pm uninstall -k --user 0 com.samsung.android.email.provider
pm uninstall -k --user 0 com.android.chrome
pm uninstall -k --user 0 com.google.android.gm
pm uninstall -k --user 0 com.google.android.googlequicksearchbox
pm uninstall -k --user 0 com.samsung.android.game.gamehome
pm uninstall -k --user 0 com.samsung.android.arzone
pm uninstall -k --user 0 com.sec.android.app.sbrowser
pm uninstall -k --user 0 com.samsung.android.spayfw
pm uninstall -k --user 0 com.samsung.android.authfw
pm uninstall -k --user 0 com.samsung.android.samsungpass
pm uninstall -k --user 0 com.android.vending
pm uninstall -k --user 0 com.google.android.gms
pm uninstall -k --user 0 com.google.android.youtube
pm uninstall -k --user 0 com.google.android.setupwizard
pm uninstall -k --user 0 com.samsung.android.ardrawing
pm uninstall -k --user 0 com.samsung.android.ardrawing
pm uninstall -k --user 0 com.samsung.android.visionintelligence
pm uninstall -k --user 0 com.sec.android.app.chromecustomizations
pm uninstall -k --user 0 com.android.egg
pm uninstall -k --user 0 com.android.providers.partnerbookmarks
pm uninstall -k --user 0 com.microsoft.appmanager
pm uninstall -k --user 0 com.android.hotwordenrollment.xgoogle  
pm uninstall -k --user 0 com.android.hotwordenrollment.okgoogle  
pm uninstall -k --user 0 com.samsung.android.bbc.bbcagent
pm uninstall -k --user 0 com.samsung.android.aremoji
pm uninstall -k --user 0 com.samsung.android.bixby.agent
pm uninstall -k --user 0 com.samsung.android.bixby.agent.dummy
pm uninstall -k --user 0 com.samsung.android.bixby.service
pm uninstall -k --user 0 com.samsung.android.bixby.wakeup
pm uninstall -k --user 0 com.samsung.android.game.gametools
pm uninstall -k --user 0 com.google.android.partnersetup
pm uninstall -k --user 0 com.google.ar.core
pm uninstall -k --user 0 com.samsung.android.app.galaxyfinder
pm uninstall -k --user 0 com.samsung.android.app.spage
pm uninstall -k --user 0 com.google.android.apps.restore
pm uninstall -k --user 0 com.google.android.onetimeinitializer
pm uninstall -k --user 0 com.google.android.apps.turbo
pm uninstall -k --user 0 com.samsung.android.game.gos
pm uninstall -k --user 0 com.sec.android.service.health
pm uninstall -k --user 0 com.samsung.android.easysetup
pm uninstall -k --user 0 com.samsung.android.beaconmanager
pm uninstall -k --user 0 com.samsung.android.smartswitchassistant
pm uninstall -k --user 0 com.sec.android.easyMover.Agent
pm uninstall -k --user 0 com.samsung.android.shortcutbackupservice

```

## Reinstalling an App

To Reinstall:

```
adb shell cmd package install-existing <package_name>
```

## Installs

Install [F-Droid](https://f-droid.org/) (move APK over from host)

### via F-Droid

* Install DuckDuckGo
* Aurora Store
* Breathly
* warpinator
* Tutanota
* Interval Timer(privacy friendly)

### Via Aurora store


#### Via no Aurora Store: No Security
