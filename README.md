# Procedural Jellyfish

## Animation




<img width="1280" height="720" alt="Jellyfish1" src="https://github.com/user-attachments/assets/97c5df76-3a8f-4600-813f-d05755ecfed7" />

## Renders

<img width="1280" height="720" alt="Jellyfish1" src="https://github.com/user-attachments/assets/cdc7c19e-2210-4f46-9c7a-6de2fd9426e3" />
<img width="1280" height="720" alt="Jellyfish2" src="https://github.com/user-attachments/assets/b8897129-2749-4fd5-b24c-5330e4854e2a" />

## Description

I procedurally generated a Jellyfish using Houdini. There are 5 geometry instances:
- The main body
    - This was created using a line and bend nodes. I revolved it around the scene to create a dome shape for the jellyfish body, and add some light terrain fractals to create a more organic shape in the jellyfish. I also animated the body as well.
    - <img height="600" alt="body" src="https://github.com/user-attachments/assets/f4d75c5c-742f-4cc7-b469-8955da220b5a" />

- The frilly strings
    - Started off with a grid node and then used a custom VEX script to create a ruffle-like shape to the grid, then a twist node for more frilliness. Afterwards, I attach it to the jellyfish's body and inherit its animation. The strings follow a Vellum cloth solver. Each string is duplicated and rotated around the body four times.
    - <img height="600" alt="stringsfrill" src="https://github.com/user-attachments/assets/7fb6cd85-c649-4ed2-8be1-65d109cced11" />

- The outside, spaghetti-like strings
    - Similarly to the frilly strings, these strings use a Vellum cloth solver. I attach it to the rim of the jellyfish's body, one string per vertex of the body in the rim.
    - <img height="600" alt="strings" src="https://github.com/user-attachments/assets/7ecfbde1-0246-4c65-a2d8-475eca8e7ede" />

- The organs
    - The organs are procedurally generated using a curve and sweeping to generate a mesh. I bend, and add some terrain fractals to make the shape appear more organic. Then, I duplicated the organ four times around the center of the jellyfish and attached it to the body's animation.
    - <img height="600" alt="organs" src="https://github.com/user-attachments/assets/ae32fe6c-9921-4f27-a002-dcd43819b0ec" />

- The veins
    - I took the body and remeshed it - then used a shortest path node to create a path between a given vertex in the jellyfish's remeshed body to another vertex. I smoothed out the paths, then used a sweep node to create a mesh along the spline. I attached to the jellyfish's body animation.
    - <img height="600" alt="veins" src="https://github.com/user-attachments/assets/6f7b67b4-adc1-4270-8c0d-f6caf2d5d8f9" />

