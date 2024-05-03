Welcome to the follow-up of the main guide for using your model in VRChat! There won't be much more work to be done from here, but I decided that it was best practice to have this info in a separate place. This guide will pick up from the work in Unity in the [main guide](</Guides/Main Guide.md>).

# Resources

- If you didn't get it before, you need the [VRChat SDK](https://vrchat.com/home/download).
- As a matter of preference, you may want to use a [Rero Shader](https://github.com/RetroGEO/reroStandard/releases).
- If you want to go hard in designing your avatar, consider using the [Dynamic Bone script](https://assetstore.unity.com/packages/tools/animation/dynamic-bone-16743).

# Materials

The main guide glossed over this step, so let us tackle this now. The Rero shaders are linked above, but the specific shaders you use will be both a matter of preference and what you can get working.

1. First, select all the materials you extracted in your Unity project. 
2. Set the shader of these materials to the specular shader of your choice. By default, Unity has "Standard (Specular setup)." You may also use the Rero Standard (Specular setup) shader.
3. Set the Rendering Mode to Cutout. 
4. For each material, assign their respective emissive and specular textures. Additionally, set the Smoothness and Alpha Cutoff parameters until they are to your liking.
	- For the Facial Features material (the material usually labeled "etc"), consider using the Fade Rendering Mode.
	- For the Eye material(s) (the material usually labeled "iri"), you may find that the Specular texture makes the eyes overly reflective. In that case, consider using the Diffuse texture where the Specular texture would normally go.
	
# Avatar Descriptor

Now we have to set some settings for the avatar for VRChat to use.

1. In the scene, select the Avatar and hit Add Component, then select VRC Avatar Descriptor.
2. First, we will set the view point. This determines where the camera is positioned in-game, and is represented by a small white ball that has appeared in your scene. In the Avatar Descriptor, adjust the coordinates of the View Position parameter until it is eye-level, centered in your character, but can preferentially be inside the head or right in front of it.
3. Open the LipSync dropdown menu, and change the mode to Viseme Blend Shape. Select the mesh that the shapekeys are assigned to, and it should auto-populate the visemes created by Cats.
4. In the Eye Look dropdown, click Enable. The Calm-Excited and Shy-Confident sliders affect how often and how long your model's eyes will lock onto targets. Adjust as you like.
5. Input the `j_f_eye` bones as appropriate in the Transforms list. Under Rotation States, adjust the rotations of the eyes until they look in the desired directions. You can do this by hitting Preview and rotating the eyes in the scene.
	- Keep in mind that instances of left and right here use your character's left and right, not yours.
6. Under Eyelid Type, select Blendshapes and select the mesh that contains your shapekeys. For Blink, input your blink shapekey. Leave Looking Up/Down empty.

And that's all the direct interfacing that you strictly need to have done with your model! Just a few things left.

# VRChat Control Panel

This is where we get your model ready for publishing.

1. At the top, choose VRChat SDK > Show Control Panel.
2. Sign in to your VRChat account.
3. Go to the Builder tab. If there are any red errors, the Auto-Fix button should get that settled for you.
	- For good measure, go over any of the other warnings/messages the Control Panel may have for you to make sure none are too serious.
4. Scroll down to Online Publishing, and hit "Build & Publish for Windows." 
	- If the Publish button is greyed out, consider looking into the [VRChat Trust System](https://docs.vrchat.com/docs/vrchat-safety-and-trust-system). TL;DR: play more.
5. Fill out the avatar information in your Unity Scene and hit Upload.

And just like that, your model should upload to the game! Have fun!