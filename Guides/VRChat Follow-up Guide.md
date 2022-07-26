Welcome to the follow-up of the main guide for using your model in VRChat! There won't be much more work to be done from here, but I decided that it was best practice to have this info in a separate place. This guide will pick up from the work in Unity in the [main guide](</Guides/Main Guide.md>).

# Resources

- If you didn't before, you need the [VRChat SDK](https://vrchat.com/home/download).
- As a matter of preference, you may want to use a [Rero Shader](https://github.com/RetroGEO/reroStandard/releases)
- If you want to go hard in designing your avatar, consider using the [Dynamic Bone script](https://assetstore.unity.com/packages/tools/animation/dynamic-bone-16743).

# Materials

The main guide glossed over this step, so let us tackle this now. The Rero shaders are linked above, but the specific shaders you use will be both a matter of preference and what you can get working.

1. First, select all the materials you extracted in your Unity project. 
2. Set the shader of these materials to the specular shader of your choice. By default, Unity has "Standard (Specular setup)." You may also use the Rero Standard (Specular setup) shader.
3. Set the Rendering Mode to Cutout. 
4. For each material, assign their respective emissive and specular textures. Additionally, set the Smoothness and Alpha Cutoff parameters until they are to your liking.
	- For the Facial Features material (the material usually labeled "etc"), consider using the Fade Rendering Mode.
	- For the Eye material(s) (the material usually labeled "iri"), you may find that the Specular texture makes the eyes overly reflective. In that case, consider using the Diffuse texture where the Specular texture would normally go.