If you plan to use an outfit for your Hrothgar that would expose bare skin where fur would appear, you'll want to follow this guide in addition to the main guide. We will be modifying your Hrothgar's diffuse body texture to include the fur. The only additional tool you'll need is some image editing program such as Photoshop.

1. In TexTools, navigate to Character > Body > Hrothgar Male (or Female) > Textures.
2. Under the Materials dropdown list, browse through the "A" materials and select "Multi" under Texture Map. You will find an image that is predominantly red, yellow, and white. Search through these "Multi" textures until you locate the pattern that resembles your own. If you have no pattern, any of these will do. Export it.
3. In Photoshop, open the Multi texture you just found.
4. Open the Channels panel, and click the Green channel. Press Ctrl+A and Ctrl+C to Select All and Copy. Click RGB to reselect all channels.
5. Back in the Layers panel, create a new Solid Color layer, and choose the colour that corresponds to your fur (not the fur pattern) using the exact colour picked from your references at character creation.
6. Alt-Click the layer mask (the white rectangle on the right of the solid colour you chose) and press Ctrl+V to Paste. You should now see the proper fur colour overlaid onto the Multi texture. Hide the Solid Color layer.
7. If your character has a fur pattern, repeat steps 4-6 using instead the Blue channel rather than the Green channel. The colour of the Solid Color layer should be that of the fur pattern this time.
8. Import as the base layer into Photoshop the originally-exported Diffuse texture for the body, hide the Multi layer, and show the two Solid Color layers. You should now see the diffuse layer as if your Hrothgar's fur is properly laid onto it.
9. Export the result.

The process should look like this:
![Hrothgar fur image editing](/assets/Luggs/hrothfur.gif)

Congratulations! You should now have a new texture to serve for the bare body of your character for future outfits. Make sure to replace it for the new Diffuse texture for the appropriate material in Unity.

Thank you to Graphic Design Stack Exchange user Wolff for the help in solving this problem!