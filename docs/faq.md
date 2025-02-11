﻿import RadioButtonCheckedIcon from '@mui/icons-material/RadioButtonChecked';
import RadioButtonUncheckedIcon from '@mui/icons-material/RadioButtonUnchecked';

# Frequently Asked Questions

---

### Application Load Error 5:0000065434

Run your game directly through Steam once. You may also need to restart Steam and/or Mod Organizer 2. If that still doesn't work, place a copy of your Steam.exe (a copy, not a shortcut) into the game's [Root](https://thebestoftimes.moddinglinked.com/setup.html#terms) folder.

### Can I add _mods X Y and Z_?

<details>
<summary>Short answer: No.</summary>
<p>Long answer: Well, it depends. No one can tell you with certainty that it is 100% safe to add a mod. Compatibility generally isn't a yes or no question. If you are an experienced modder and understand that many mods will require patching in xEdit and that you will need to manually sort it in your load order, then yes you can probably add that mod. If you are a beginner and don't know how to do any of that, you should not add any mods. Essentially, if you have to ask if you can add a mod, you probably shouldn't.</p>
</details>

### Can I use Vortex?

<details>
<summary>Short answer: No.</summary>
<p>Long answer: The guide is oriented completely towards MO2 and takes advantage of a number of its exclusive features. You should use whatever mod manager you like, but we are unable to accomodate Vortex users looking for support, as none of us use it. If using MO2 is a dealbreaker for you, we recommend <a href="https://youtu.be/Zts-tF0nYIk" target="_blank">Gopher's video tutorial</a> instead of this guide.</p>
</details>

### DarN instead of VUI+

If you want to use [DarNified UI](https://www.moddb.com/mods/unofficial-darnified-ui-update)
instead of Vanilla UI Plus, you will need to make the following changes:

- Reinstall [Clean Vanilla HUD](ui#clean-vanilla-hud) with these alternative settings:
  - Main Mod:
    - [x] Main Files
    - [ ] Clean Fonts
    - [x] Clean Map Icons
    - [ ] Clean Radiation Bar
    - [x] Clean Shared Interface
  - Clean Roulette Loading Wheel:<br/>
    <RadioButtonUncheckedIcon fontSize="small" /> Loading Roulette Wheel<br/>
    <RadioButtonUncheckedIcon fontSize="small" /> Loading Roulette Wheel HD<br/>
    <RadioButtonCheckedIcon fontSize="small" /> None above<br/>
  - Patches:
    - [ ] Vanilla UI+ Patch
    - [x] I am not a Height Indicator User
    - [x] Alternative Just Hit Indicator
    - [x] Clean Fonts for DarnUI
- Uninstall the following mods as they aren't compatible with DarN UI:
  - [Clean Vault Boy Paper Doll](ui#clean-vanilla-hud)
  - [Three-perk Bounty](overhauls#three-perk-bounty)

### Game runs too fast

If your game is moving too fast, double-click New Vegas Tick Fix (NVTF) and use the **INI Editor** tab to make sure **iMaxFPSTolerance** is set to **500** in `NVTF.ini`. If that still doesn't fix it, verify that NVTF is actually working by using the console command `IsDLLLoaded NVTF`.

### I found a mistake in the guide

Please click the "Edit this page" link at the bottom of the page on the left. It will allow you to [fork the guide and submit a pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) with your changes. Thanks for helping out!

### `loadorder.txt` has mods I didn't install

No need to worry; this is actually intentional. MO2 parses the file line-by-line and compares it to your modlist, and when any given mod is missing, MO2 simply skips it and goes to the next line. The mods that _are_ present will be ordered correctly and anything absent will be ignored. Some mods that were included in older versions of the guide, or other popular mods which may cause problems with mods in the guide if they were in the wrong place, are therefore included in the file to cover edge cases or outdated . This is no cause for concern. As is stressed in the comments at the top of the `loadorder.txt``, there's no need to read or modify the file.

The only time the loadorder.txt might fail to properly order your mods is if you added mods on your own that aren't in the guide. Those mods will need to be manually reordered to the appropriate spot in your loadorder, so if you aren't familiar with how to the correct spot, how to make patches in xEdit and so on, then it may not be a good idea to add additional mods.

### Merge, Rename, Replace?

When installing multiple mods from the same page through MO2, you should **Rename** to the **file name** of the file you downloaded, as described in [The Best of Times](https://thebestoftimes.moddinglinked.com/mo2.html#installation_instructions).

### MO2 reports overwritten loose files

MO2 reporting overwritten loose files is fine. As long as your mods in the **left** pane of MO2 are in the exact order as they appear in the guide, these overwrites are intentional and safe.

### MO2 reports files in Overwrite

MO2 reporting files in overwrite is not a cause for concern. These are usually files generated by mods (like configuration INI files) or by programs ran through MO2. These files will still be loaded fine in-game, and will be prioritized as if they are the last mod in the left pane of MO2. Usually, you can just leave these files in the overwrite and ignore the warning. If you like, you can drag the files out of the Overwrite window into their respective mod folders in MO2's left pane.

### No DLC pop-ups on new game

- [Delay DLC Redux](gameplay#delay-dlc-redux-ttw) prevents the DLC pop-ups from showing until you reach the starting location for the DLC. Read the description!
- [SawyerBatty](overhauls#sawyerbatty) distributes the crap pack items throughout the DC wasteland (or NV depending on where you chose to start).
<details>
<summary>SPOILERS: SawyerBatty DLC pack locations for Capital Wasteland</summary>
<p>Caravan Pack - Basement of Red's house in Big Town<br/>
Classic Pack - Trunk of a car South of Megaton<br/>
Mercenary Pack - Talon Outpost South West of Megaton near Grayditch<br/>
Tribal Pack - Back porch of house near Springvale School</p>
</details>

### Ultrawide resolution

In MO2, open **Tools > INI Editor** and make sure you are in the **FalloutCustom.ini** tab and NOT the **Custom.ini** tab. Add the following lines:

```ini
[Display]
; Ultrawide support
iSize W=3440
iSize H=1440
```

Then, in-game, go to Settings/Tweaks and type "ultrawide" in the search bar. Enable the Ultrawide Support tweak by clicking it in the panel on the lefthand side, then exit and restart the game so it takes effect.

### What do these installation instructions mean?

Review [The Best of Times](https://thebestoftimes.moddinglinked.com/mo2.html#installation_instructions) for how to install mods in MO2.

### Why isn't _mod X_ in the guide?

Because modding guides reflect the preferences of their authors.
