# Introduction

Welcome to the first part of the guide. No matter your aim in undertaking this project, you'll first have to bring your Warrior of Light to Blender, the free and open-source 3D Modeling software. Luckily, this step has become *significantly* easier thanks to recent developments.

# Disclaimers

Working with 3D software is not easy. You may find later down in the process that you'll have to revisit Blender to make adjustments or add more features. It happens (and it's frustrating). That said, I have a few things for you to keep in mind:

First, our objective with this guide will be to port one "appearance" for your Warrior of Light. That is, we will assume one set of customizations for your character (as determined in Character Creation/the Aesthetician), and one outfit. Combining multiple appearances to use with one model is beyond the scope of this guide.

Secondly, **save**. Often. 3D software is very... shall we say, sensitive. There is a lot that can go wrong. With that in mind, you should make a new save of your Blender project after basically every step. You will almost certainly run into cases where you'll have to undo so many steps that it goes beyond Blender's history limit. We want plenty of saves to reload in case you make a mistake. Yes, this does mean you'll lose progress. I'm sorry in advance.

Third, not everyone's needs are the same. By extension, not everyone will need to follow the same advice. To that end, I will be making use of GitHub's "Alerts" to point out when some users will have to follow different instructions than others. The people intended to read the Alert will be noted at the beginning. Here is one for modders, both as a form of advice, and to know what to look out for.

> [!WARNING]
> **For modders:** This process is ostensibly mod-compatible. That is, mods that affect your character's or their gear's appearance should function properly with this guide. However, I can't guarantee compatibility for non-standard skeletons or other kinds of mods. I can guarantee that VFX mods will not be reflected. Though Meddle does have support for capturing animations, this will not be covered by this guide.

# What You'll Need

- Access to your account via PC.
	- That is, you'll need to either have a Free Trial account or active subscription on PC or Steam.
	- Technically, if you have an unmodded character, you only need access to your character - creating a Free Trial account if you're a console-only player is an option in this case.
- A fresh directory to store all your project files. This serves two purposes:
	- First, organization. This project will span many different types of files from all around your computer. It's best to have them in a centralized spot on your computer to find again later.
	- Second, protection. Blender files contain links to their source information, rather than keeping their own copies. So if you try to use the same files for two projects, and then move or edit one, the other will get unlinked, and this will cause headaches down the line if you do not plan for it.
- [XIVLauncher and Dalamud](https://goatcorp.github.io/).
	- [The Meddle Plugin](https://github.com/PassiveModding/Meddle).
- [Blender](https://www.blender.org/). Get the most recent version.
	- [The MeddleTools addon](https://github.com/PassiveModding/MeddleTools).

> [!IMPORTANT]
> **For Customize+ users:** You'll also need [Bustomize](https://github.com/sleepybnuuy/bustomize).

More may be required depending on your use case.

# Step 1: Setup

>[!TIP]
> **For modders:** If you mod, you're likely familiar with this step. Feel free to install Meddle as you would any other plugin that's not in the main listing, then move on to Step 2.

Download and install XIVLauncher, as linked above. You'll want to make sure to enable the Dalamud framework during the installation. You'll have to log in - this should be secure, as Dalamud does not store your password itself - it is stored with Windows Credential Manager (at least, on Windows).

Once the game is launched and you've logged in to your character, enter the command `/xlplugins` into chat. This will bring up Dalamud's plugin installer. In the bottom left, click `Settings` and navigate to the `Experimental` tab. Scroll down until you reach the section `Custom Plugin Repositories`. 

Locate the Repository URL in the page for Meddle - it'll be located in the `Installation` section. Copy that URL and return to the game. Input that URL in the first open space for custom plugin repositories. Hit the `+` icon to its right, then hit save in the bottom right.

Search the plugin installer for Meddle, click it, and install it.

# Step 2: Meddle

Have the desired character achieve their desired appearance.

> [!NOTE]
> **For modders:** You don't need to do anything special here. If you go onto a modded outfit or modded body, they should still be reflected in the export. As warned earlier though, be ready to anticipate that there may be issues with certain kinds of mods.

Enter the command `/meddle` into chat to open the Meddle interface. Under `Select Character`, make sure the desired character is chosen. Characters will likely be ordered by distance to the player character, and therefore the player character should always be first on the list for convenience.

For the first section, `Character`, click `Export All Models with Attaches`. Use the default settings, but make sure most of all that `Pose Mode` is set to `Reference Pose with Scale`. Once you hit Export, it'll prompt you to choose the path you save it in (and by default will open that folder afterwards). What matters is you copy the export after the fact to your dedicated directory after this.

# Step 3: Blender

Start up Blender. Feel free to click on the default cube in the "Viewport" ( this is where the 3D models will appear) and hit Delete on your keyboard to delete it. Hit `Ctrl+,` to open up the Add-ons menu for Blender. At the GitHub page for the MeddleTools Add-on, download the newest Release on the right-hand side. It'll be the `.zip` file.

Back in the Add-ons window, click the small dropdown in the top right, and choose `Install from Disk...`, and navigate to the zip file for MeddleTools. It should now appear in the list. Make sure it is enabled.

While your cursor is in the Viewport, hit N to open the `N-menu`. You will see a couple of options appear. On the right side, click `MeddleTools`. You should not need to adjust any settings. Under `Meddle Import`, click `Import .gltf/.glb`, and navigate to the `.gltf` file in the Meddle export from Step 2. Select it, and hit `Import Model`. 

Your Warrior of Light should appear, if very white. To see them in full colour, look at the top right of the viewport. You'll see four sphere icons, with the second selected. Click the third, and they should be properly coloured.

> [!IMPORTANT]
> **For Customize+ users:** It's time for a Bustomize detour. Download and Install the Bustomize Add-on exactly as you did with MeddleTools. In the N-menu, there should now be a `bustomize` section just as there was for MeddleTools. For `Target Armature`, there should only be one option for your exported Character. Select it. 
> 
> Now we need your `Customize+ String`. Back in game, open up the Customize+ menu. Locate whichever Template is being applied to the character. If currently two or more are being applied as part of one Profile, you'll need to consolidate them somehow into one template. I'm sorry to say there is not an easy way to do this.
> 
> Once you have your template, select it, and then look to the left if its name in the upper bar. You'll see a button called `Copy the current template to your clipboard`. Click it, and then paste it as the Customize+ String in Bustomize. You may now click the `do bustomize` buttons, though most likely you'll only need to click the one that reads `(scale)`. If clicking the `(rot, pos)` button messes up the model, click `reset armature` to fix it and only use the (scale) button next time.
# Where to Next

At this point, we reach our first proper split. As of me writing this, there are three primary paths that I can conceive of for a model at this stage to go:
- To Unity,
- Staying in Blender, or
- To a 3D Printer.
Each of these three trajectories are rather different, and so I'll address them in turn.

## Unity: VRChat Avatars and VTuber Models

You folks (whom I assume are the most frequent visitors of this guide) have rather large roads ahead. Your jobs will be to further edit your model to be compatible with Unity, and by extension, your respective software. 

However, I cannot anticipate that these processes will overlap significantly. Therefore, I will split what comes next for your two groups into separate guides. I personally can only assist with the process for building a VRChat model. Expect the VTuber model guide to stay unmade until a volunteer can provide further instruction.

The follow-up guides will be available at:
- [[Blender to Unity for VRChat]], and
- [[Blender to Unity for VTubing]].

## Blender: Animation and Archival

You guys are almost done. There's just a bit of hooking up to do. Specifically, you'll have to deal with fixing non-functioning materials and meshes, and connecting attachments (think weapons, fashion accessories, mounts).

If and when such a guide is made, it'll be found at [[Fixing Models to Stay in Blender]].

## 3D Printing

Honestly, you're basically done. Since a 3D-printed model isn't in need of detail beyond the shape of the model, you don't need to care about materials or anything. All that's left for you is to pose the model, then send it off to your Slicer software before going to the printer.

There's not much use in writing a guide for you because:
1. You probably already know how to do this, and
2. The process varies by slicer and printer enough that what guidance I have to give wouldn't be helpful.