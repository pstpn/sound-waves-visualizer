# Sound Waves Visualizer

Visualizer of sound wave propagation in a closed space. A wave is emitted from a point source as an expanding sphere; each point of the wave moves at a given speed and reflects when it hits the room walls or obstacles placed in the scene. The scene is rendered with OpenGL in real time, and the simulation is controlled through an ImGui interface.

## Features

The wave source, its speed and color are configured in a dedicated menu; obstacles are placed, scaled, rotated and recolored freely, and the lighting (position and color of the light source) is adjusted with Phong shading. The camera is free-fly with mouse look and WASD movement.

## Tech Stack

C++, OpenGL 3.3 Core, GLFW, GLAD, GLM, Dear ImGui. Models are loaded through a custom OBJ loader.

## Examples of Work

Waves in an empty room:

![Waves only](doc/SEN/inc/img/demoonlywaves.png)

Waves with obstacles:

![Waves with obstacles](doc/SEN/inc/img/demowithobst.png)

## Performance

Frame generation time measured with an increasing number of obstacles (Intel Core i5-10300H, NVIDIA GeForce GTX 1650, Ubuntu 22.04):

| Obstacles | Frame time (µs) |
|-----------|----------------|
| 1 | 3.241 |
| 2 | 6.112 |
| 3 | 9.445 |
| 4 | 13.567 |
| 5 | 17.131 |
| 6 | 21.522 |
| 7 | 25.525 |
| 8 | 29.332 |
| 9 | 34.124 |
| 10 | 37.746 |

## Documentation

The full coursework documentation is available in the `doc/` directory (in Russian).

## Build

Open `reborn/CourseWork/CourseWork.sln` in Visual Studio and build. The dependencies (GLFW, GLAD, GLM, Dear ImGui, assimp) are not in the repo and are expected next to the solution, as `.gitignore` suggests.