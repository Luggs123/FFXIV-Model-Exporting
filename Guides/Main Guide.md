Welcome to the main guide for exporting your FFXIV character into a 3D model! This part of the guide will cover what nearly every player model will require. Note that some characters may require additional steps that take place during this guide. Please browse through the Specialized Guides and find any that apply to you.

# What You'll Need
- An active FFXIV subscription
- [TexTools](https://www.ffxiv-textools.net/)
- (Optional) An in-game appearance editor, such as [Anamnesis](https://github.com/imchillin/Anamnesis).
- An image editor, such as Photoshop or [GIMP](https://www.gimp.org/downloads/)
	- (Optional) A downloadable screenshot program such as [Gyazo](https://gyazo.com/download), just for taking cropped and convenient screenshots with little to no extra information.
- [Blender](https://www.blender.org/)
	- [Blender Cats plugin](https://github.com/absolute-quantum/cats-blender-plugin)
- [Unity](https://unity.com/download)
	- For VRChat purposes, you want Unity version 2019.4.31 and the [VRChat SDK](https://vrchat.com/home/download)

# Advisories
I *highly* recommend that you save extremely frequently. Not just normal saves, either; **save a new copy** every time you complete a major step in this process. Especially if this is your first time working with 3D content, you will likely find yourself making mistakes, worst of all towards the beginning. If you don't save often, you will find yourself starting over many times. So keep a folder full of saves of your project at all of its stages. Preferably keep them numbered, but as long as you can tell what step a given save is at, you should be fine. 

In general really, you should keep your project organized. This project requires many different programs with many different file types and save locations. You want it to be as intuitive as possible to find where everything is located. This can take the form of a document with vital information, or a well-laid-out folder that contains everything for your project.

# Step 1: Gather References
## Step 1a: Character Appearance

First, we need to obtain your character's appearance data. This is all the data pertaining to character creation or the aesthetician. We'll be taking many screenshots here, so it's vital you have a folder ready to store them in.

Repeat this process for each different character you'll make.

1. If your character appearance isn't already saved, locate them from the character selection screen. Right-click their name and select "Save Appearance Data," and save them to a slot.
2. Create a new character, loading their appearance data.
3. Go through each category, taking a screenshot of the options and what you've chosen. Title each screenshot with the category and the setting (if applicable).
	- This includes your race and clan. While your race should be obvious enough, your clan may be relevant later.
	- You can skip Height. If you care about that, check Step 1b.
	- If the option has you choose *exactly one* option from several image previews, its setting will be its position in the list, skipping any "none" option. Examples are Face, Hairstyles, etc.
		- If you use a hairstyle that is unlocked in-game using a copy of *Modern Aesthetics*, there is not necessarily an easy way to figure out your setting number.
		- For options where you can choose multiple, screenshot as normal. Examples are Tattoos and Face Paints.
	- For colour selection options, it is vital that the Previous/Current previews be visible in your screenshots. We will need those exact colour values. Examples are Skin Color, Eye Color, etc.
	- For options where you pick from a list (most often Type 1, Type 2, etc), its setting will be "None" for the first option, "A" for the second option, "B" for the third option, and so on. Examples are Eye Shape, Nose, Eyebrows, etc.
		- Voices are beyond this guide's scope.
4. You can now exit out of character creation.

You should now have a folder of screenshots containing all the character creation info for your character.

## Step 1b: Outfits

Next, we need to gather info for the gear your character will wear. Weapons, in both your main- and off-hands, are beyond the scope of this guide.

1. Prepare a text document or other scheme for saving and organizing your outfits.
2. For each outfit, write down the full details in your document. You'll want to know the equipment name and, if applicable, the dye applied to it.
	- Empty gear slots can be omitted.

Some notes:
- Though not necessary, it can be helpful to take reference screenshots here too. If you choose to do so, take them not only of the equipment model, but also the dye colour as shown on the gear icon.
- These outfits don't have to be ones you've acquired yourself - you can use Anamnesis (as mentioned above) to preview items and dyes you don't have on your character.
- If your character height is important to you, then while logged in open Anamnesis and move to the appearance tab. On the right, in the Model block, note down the height. Do not use the number in the Customize block - you want a number from 0 to 1.

# Step 2: TexTools

This step deals with the extraction process. We'll be using TexTools to gather all the 3D assets that pertain to your model.

## Step 2a: Preparation

Before we do any of the heavy lifting with TexTools, we want to prime it for what's to come. Specifically, we'll be preparing it for your character, so you will have to repeat this process if you begin working on a different character.

1. In TexTools, go to Options > Customize.
2. Make note of the Save Directory - this is where your 3D models will appear.
3. Open your image editor and import your screenshots with colour choices. Grab the hex values for your choices using the dropper tool equivalent, and in TexTools insert those hex values under the Colors & Skins section as appropriate. 
	- If your character doesn't have highlights, match them with their hair colour.
	- If your character doesn't have a lip colour, match it to their skin colour.
	- If your character has heterochromia (or "odd eyes," as the game calls them), set the iris color to that of either eye.
4. Hit Close.

## Step 2b: Building Your Character

This process will use TexTools' Full Model Viewer (FMV), which you can access from TexTools at any time via Tools > Full Model Viewer. Be aware that **mods installed through TexTools will be reflected, but mods installed through Penumbra will not**. If this is an issue for you, install or uninstall those mods as needed. Keep the Item List as "By Category" for this whole process.

### Step 2bi: Face & Hair

1. Go to Character > Face, and choose your Race/Gender option.
2. Go to the Models tab.
3. Find your character's face under the "Number" dropdown. 
	- In most cases, your face number will correspond to the setting scheme laid out in Step 1a. However in some cases (such as Hrothgar Males post-6.1), the faces may appear multiple times. Consult any relevant racial guides if you find this is the case.
4. Click "Add to FMV."
5. Next, add the Hair just as you did the Face.
	- For unlockable hairstyles, you will have to search through the list TexTools provides. As a rule of thumb, default hairstyles begin from 1 and continue in consecutive order, while unlocked hairstyles begin after a large gap.
	- Similarly, in some cases the association laid out in Step 1a will not function perfectly. Once again, please consult any relevant racial guides if this applies.

### Step 2bii: Racial Features

Depending on your race, you may have to add the following:
- For Miqo'te, Au Ra, and Hrothgar, add your Tail.
- For Viera, add your Ears.

### Step 3biii: Equipment

1. Locate each piece of equipment in your outfit in TexTools in the Item List. 
2. Change the race to your own.
	- Depending on your race, you may find that most gear will not explicitly list your race here - this is because many races share models. In general, Hrothgar share models with Roegadyn; Female Lalafells might use Male Lalafell models; and Elezen, Au Ra, Miqo'te, and Viera will use the Hyur Highlander models of their respective gender.
3. If the given piece of equipment is dyed, go to Textures and the texture map to ColorSet. If your race does not have a ColorSet texture map, change the race to either Hyur Highlander Male/Female, depending on your character's gender and the item.
	- Go through each row of the ColorSet (click them manually; the Up/Down arrows are used to switch the positions of two rows) and for each with a Dye Template attached, choose the dye you want to apply from the "Preview Dye #" dropdown on the right, then hit "Copy Dye Values to Row." Hit Save.
4. Choose Models, and change the race/gender to your own. Press "Add to FMV."
5. If you modified the ColorSet above, return there and press Disable at the bottom. This will return the equipment to its unmodified state.
6. Repeat the above steps until you have added all the equipment pieces for your outfit.

## Step 3c: Exporting

From the FMV, make sure the Skeleton and (if applicable) Face options are properly set on the top bar. Once they are, hit Export at the bottom. Give your export a name, and it will produce all the 3D components of the character you built.

If your character has heterochromia, we will take the opportunity to export that now. Return to the customize menu and replace the iris color with that of the other eye. Once that's saved, you can return to your race's face and add that to the FMV, replacing your previous face. Feel free to delete all other components of the model to better distinguish this from the main model you just exported. Export this new face.