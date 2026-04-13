# Unity-Object-Space-Normal-Shader (Hand painted effect)
This project includes a Unity Engine Shadergraph supporting Object Space Normal Painting.
It allows for handpainted looking shadows, by drawing onto a normal map and using this Shader.
It is based on this blender tutorial: https://www.youtube.com/watch?v=s8N00rjil_4&t=263s
<img width="2000" height="907" alt="FromTo" src="https://github.com/user-attachments/assets/ad7871b8-2298-4142-ba38-d6a044e29e69" />

# Install
- Download the package by clicking the green Code Button and download the zip (or just use the package manager)
- Drag and drop the package into your project.
- Open the "PaintingEffect_DemoScene"

# What you need 
For the Shader to also work on your own Meshes, please follow these steps
- Make sure your UVs don't overlap, even for symmetrical Meshes
- Bake an Normal Map in Object Space for your Mesh, I used Blender for example.
- You can edit this texture to showcase your brushstrokes (example below)
- When importing the Texture to Unity, disable sRGB
- You can now use the "M_ObjectNormals" with the texture you created
 <img width="2048" height="1024" alt="BakedNormals" src="https://github.com/user-attachments/assets/a34734ef-8348-48c6-907d-4a0cd3cd0ead" />

 # Animated Brushstrokes
Additionally I included a VFX Graph that adds brushtrokes to the object over time.
The animated brushstrokes uses VFX Graph Particles that samples your Object Normal Texture and spawn Brushstrokes onto a RenderTexture. Finally this gets used by the Shadergraph.
- Use the M_LiveObjectNormals
- It is controllable through the "Stroke_VFX" gameobject
- You can use a RGB Texture to indicate where Brush strokes shall be bigger/smaller and more/less.
![PaintGif](https://github.com/user-attachments/assets/9aca33f1-0108-4606-9a89-b445553be781)
<img width="641" height="651" alt="image" src="https://github.com/user-attachments/assets/b20f928b-9450-4ef6-bbf8-5edc691b2236" />



