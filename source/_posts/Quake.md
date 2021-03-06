---
title: QuakeSpasm on macOS
date: 2021-03-25 10:00:00
tags:
---

# Installation

Install QuakeSpasm with brew

```
brew update
brew install quakespasm
```

I wanted to install Quake to get the Id1 files to play using QuakeSpasm, but Steam won’t let me install it on Mac as it’s Windows only, so I had to do the following:

```
brew install steamcmd
steamcmd
```

You’ll now be in the steam shell.

Note that for the following to work you'll have to either log in via the Steam shell or the Steam desktop client. From here I assume that you have done so. Substitute username accordingly. 

You'll need to own Quake on Steam or this won't work.

```
login username
force_install_dir /Users/jake/.steamcmd/quake
@sSteamCmdForcePlatformType windows
app_update 2310 validate
exit
```

`@sSteamCmdForcePlatformType windows` forces SteamCMD to install Windows apps

Then you’ll need to link the Id1 folder

```
ln -s /Users/jake/.steamcmd/quake/Id1 /Applications/QuakeSpasm/Id1
```

# Mods

Unpack mods to `/Applications/QuakeSpasm`

![](Quake/quake-1.png "Applications directory structure for QuakeSpasm")

And then run QuakeSpasm and specify “game” in the command line parameters.

In my case it's `-game ad_v1_80p1final` which is the fantastical [Arcane Dimensions mod](https://www.moddb.com/mods/arcane-dimensions)

![](Quake/quake-2.png "Launch configuration for QuakeSpasm with mods")
