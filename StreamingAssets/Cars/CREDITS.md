# Model credits

Models by [Jako / fairlight51](https://sketchfab.com/fairlight51), licensed under [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/):

- [Fennec - Rocket League Car](https://sketchfab.com/3d-models/fennec-rocket-league-car-5b43b50b6eeb4a12a29671df3418f57a)
- [Octane - Rocket League Car](https://sketchfab.com/3d-models/octane-rocket-league-car-9910f0a5d158425bbc7deb60c7a81f69)
- [Ball - Rocket League](https://sketchfab.com/3d-models/ball-rocket-league-2c8911aa1dcd4c53bad842f2d354dfe2)

Changes: welded and simplified car geometry with a 0.3% mesh-radius error limit; 1024-pixel texture cap and lossless WebP encoding; removal of unused PBR maps; game-coordinate conversion; default-car matte toon shading; separated wheel animation and existing game boost effects. Original downloads retained under art-review/sketchfab-source. No endorsement by the creator is implied.

Fennec update: uses the pearl preview’s 84,823-triangle normalized model, simplified to 47,143 triangles with a 0.1% mesh-radius error limit and locked mesh borders, retaining UVs, normals and embedded textures. Wheels are split by quadrant for animation; positions are converted to the existing game envelope. The preview’s graphite rim atlas and GGX pearl/clearcoat equations are adapted for the park lighting.
# Fennec Pearl v2 baseline

The full v2 model in `fennec-v2/model.glb` is imported from the supplied Fennec Pearl v2 viewer, retaining the Jako CC BY 4.0 geometry, textures, authored normals, and baked occlusion. The untouched viewer at `/fennec-pearl-v2.html` retains its embedded credits. The compact pearl lighting atlas derives from that viewer's precomputed HDR environment.

# Vanguard reference rebuild

`vanguard/model.glb` is the complete procedurally authored vehicle geometry from the user-supplied Vanguard reference rebuild. It retains 134,408 triangles, authored normals and UVs, baked vertex occlusion, and the source material grouping. The integration separates the four wheel assemblies for gameplay animation and converts the reference coordinates to the game's existing vehicle units. It does not reuse the original Fennec vertices or textures.

# Dominus

`dominus/model.glb` is the Dominus from [Dominus - Rocket League Car](https://sketchfab.com/3d-models/dominus-rocket-league-car-f592f249a65f41cd81a0e5aa3d418cb2) by [Jako / fairlight51](https://sketchfab.com/fairlight51), licensed under [Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/). It keeps the Dominus hitbox.

# Converted car sources

`fennec`, `octane-original` and `dominus` are converted from the user-supplied FBX car sources by `Assets/Editor/CarSourceTools.cs`. The converter bakes each FBX's mesh transforms into game units, splits the wheel assemblies from the body by corner label, and embeds the source diffuse textures, so the rear lamp lenses, the source material colours and the Octane's engine map are kept. Material names, colours and the wheel corner labels are preserved for the runtime shading and wheel animation.
