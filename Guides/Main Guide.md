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
	- Yes, the eyes look bizarre. What you're seeing are the eyes for Reaper's *Enshroud* overlaid on top of the normal eyes. If you need to be reassured, the proper eyes can be seen by changing the Mesh dropdown to Mesh #2. Make sure to set it back to "ALL" afterwards.
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

# Step 4: Blender

Blender is where the meat of your work will be done. As such, I've split this section of the guide into many distinct parts to so that you don't get lost or disoriented. Once more, some advisories:

- I will reiterate my previous advice to save many backups as you progress. Not only will you make the most mistakes in Blender, but they will also be the costliest and most time-consuming without backups. 
- If you haven't already, make sure to install the Cats plugin. 
- I may reference the "viewport" - this refers to the part of the Blender window where you can see the model in a 3D environment. Some of Blender's hotkeys will only work if your mouse is inside the viewport.
- Blender is not where this guide ends, but you may decide down the line that you want to add more major features to your model. Those features will in all likelihood require working more with Blender and getting a more thorough understanding of working with it. It also means that you'll have to repeat the steps taken after leaving Blender if you choose to revisit the project.

Let's begin.

## Step 4a: Initial Actions

1. Open a new Blender project, and choose File > Import > FBX, importing the .fbx file we exported from TexTools.
2. If you like, press N while the mouse is in the viewport, scroll down to MMD Shading, and choose either Shadeless or GLSL. This will show the model with most textures applied. Your mileage may vary on the quality.
3. In the top-right, expand the orange group. Contained within are several other groups and an armature titled `n_root`. Delete all the groups (including the group everything is contained in) leaving you only with the Armature. Your model will be laying on its back.
4. Select the Armature, and go into its Object properties. Set the rotation along the x-axis to 90 degrees. Your model will be standing upright again.

## Step 4b: Bone Structure

We will briefly reconfigure the model's bone hierarchy.

Expand the Armature, and further expand the skeleton (also titled `n_root`). 
1. Select a bone, then enter Edit Mode.
2. Delete `n_throw`, `n_hara`, and `j_sebo_a`.
3. Select `j_sebo_b`, and open the Bone Properties. Set its parent bone to `j_kosi`.

## Step 4c: Deleting Meshes

Next, we will filter out any unwanted meshes. From the top of the list, we will begin with meshes that pertain to equipment.

1. Select each mesh (the orange objects labeled as "Parts") in turn. Press G and move your mouse to move the mesh around and right-click to put it back into place. 
	- For meshes that either clip or do not contribute to the model's appearance (i.e. are covered entirely by some other mesh), go to the Object Data and check if there is a Shape Key that was exported with the gear that fixes the issue. Do this by sliding the Shape Key's value back and forth from zero to one.
	- If no Shape Keys solve the issue, delete the mesh.
2. For the facial meshes, once again use G to determine the role of each mesh. Several of the meshes will correspond to your race's facial features and tattoos. Delete those that do not apply, as well as the Reaper *Enshroud* eye mesh.
3. Finally, delete the appropriate hair meshes if they clip with your headwear.

## Step 4d: Heterochromia

If your character doesn't have heterochromia/"odd eyes," proceed to the next step.

1. Change into Edit Mode and select a point on one of the eyes (preferably the eye with the wrong colour). Hit L to select the surrounding points, then P to separate the selection into its own mesh.
2. Select the new mesh and enter the Material tab. In the materials dropdown list, press the "2," creating a duplicate material for this new eye.
3. In the Texture tab, select the Diffuse texture and once again hit the "2" for the texture dropdown.
4. Scroll down to "Image" and press the "2" for the image dropdown. Then, press the file icon and import the Diffuse texture exported separately in Step 3c.

## Step 4e: Merging Meshes and Consolidation

Next, we need to merge the meshes your model needs into one. 

1. While holding Shift, select each of the Parts of your model in the hierarchy. 
2. Once all of them are selected, and with your mouse in the viewport, press Ctrl+J.

Now, we need to apply a whole bunch of your character creation selections to the model in the form of shapekeys.

3. Go to the Data tab, and scroll down to Shape Keys. In that list, you will find many shapekeys with the naming system of `shp_[part]_x`. "\[Part\]" will usually refer to some aspect of the face, and "x" will be some letter. 
4. Using the references you took all the way back in Step 1a, go through the shapekeys to find those that apply to your character by setting their value to 1. Set it back to 0 if that shapekey doesn't apply. For each \[part\], you'll only need to enable one "x."
5. For shapekeys that do apply, select them and click the arrow on the right of the list, then choose "Apply Selected Shapekey to Basis." Delete the rest using the Minus button.

## Step 4f: Making New Shapekeys

Next, we will create new shapekeys for blinking and lip syncing. Once more, an advisory: this process will be difficult to get just right. Don't be surprised if you find yourself coming back here to adjust the shapekeys we make, especially since lip syncing makes for just a vital aesthetic detail for VTuber models (and VRChat models, to a lesser extent). We'll start with blinking, just because that is a good deal simpler, and that should ease you into the process for making these new shapekeys.

Note: For blinking, you may want to repeat the process for each individual eye, especially for VTuber purposes - VTubing software will likely prefer that the eyes be rigged independently from each other. Make sure to name the shapekeys appropriately. If you do, for greatest efficiency do these steps in the following order: set one eye, set the other, revert the first eye, then revert the other.

1. Enter Pose Mode. Adjust the following bones: `j_f_umab_l` and `j_f_umab_r` for the upper eyelids, and `j_f_dmab_l` and `j_f_dmab_r` for the lower eyelids until they're closed using the Z rotation.
2. Return to Object Mode by selecting the model. Navigate to the Modifiers tab, and hit Apply as Shape Key - this will create a new Shape Key for the pose you just made. 
3. While still in the Modifiers tab, click Add Modifier, and choose Armature. For Object, choose `n_root`.
4. In the Data tab, navigate to the newly-created shapekey and rename it to "Blink".
5. Return to Pose Mode and revert the changes you made to the eyelid bones.

We are now going to prepare shapekeys for lip syncing, also known as Visemes. Precisely which visemes you need to create might depend on the application you'll use for your model. That being said, this guide will have you build three manually, then generate the rest needed for VRChat using the Cats plugin. I make no guarantees to the quality of these generated visemes - as I said above, these are difficult to get right. Worst case, you may prefer to manually make every viseme.

6. Pull up a visual reference for visemes. I do not have any specific recommendation for one to use, but [here's one such reference page for Oculus developers that I found](https://developer.oculus.com/documentation/unity/audio-ovrlipsync-viseme-reference/). 
7. Create visemes for the following sounds: "ah," "oh," and "ch." After each viseme, remember to hit Apply as Shape Key and create a new Armature Modifier. Rename the new shapekeys appropriately.
	- Optionally, hide or change the appearance of the bones that control the mouth area to better see the changes as you work.
	- Bones that control the mouth area include: 
		- `j_ago` (Lower Jaw),
		- Bones that begin with `j_f_ulip` or `n_f_ulip` (Upper Lip, depends on race), 
		- Bones that begin with `j_f_dlip` (Lower Lip) or `n_f_lip` (Oral Commissures, i.e. where the upper and lower lips meet at the sides), depending on the race.
		- Some of these bones are parents of each other. Expand the bone hierarchy for these bones.
		- You will adjust both the rotations and positions of these bones.
8. Revert the bones back to their neutral positions.
9. In the Cats plugin menu, expand the Visemes section. Input the three visemes you created in their proper spots, and press Create Visemes.
10. Still using the Cats plugin menu, scroll to the top and press Export Model.