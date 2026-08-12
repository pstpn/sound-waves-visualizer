# Sound waves visualizer

A visualiser of sound wave propagation in a closed space. A wave leaves a point source as an
expanding sphere, every point of it travels at a set speed, and when it meets a wall or an
obstacle it reflects. The scene is rendered with OpenGL in real time and driven through an
ImGui panel.

The source, its speed and its colour are set in a menu of their own, obstacles are placed,
scaled, rotated and recoloured freely, and the light can be moved and tinted with Phong
shading following it. The camera is free-fly, looking around with the mouse and moving on
WASD.

Written in C++ against OpenGL 3.3 Core with GLFW, GLAD, GLM and Dear ImGui, with a
hand-written loader for the OBJ models.

## Examples

Waves in an empty room.

![Waves only](doc/SEN/inc/img/demoonlywaves.png)

The same waves reflecting off obstacles.

![Waves with obstacles](doc/SEN/inc/img/demowithobst.png)

## Performance

Frame time as obstacles are added, measured on an Intel Core i5-10300H with a GeForce GTX
1650 under Ubuntu 22.04.

| Obstacles | Frame time, µs |
|----------:|---------------:|
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

Frame time grows linearly with the number of obstacles, since every wave point is checked
against each of them.

## Build

Open `reborn/CourseWork/CourseWork.sln` in Visual Studio and build. The dependencies are
expected next to the solution and are not kept in the repository.

The coursework text is in `doc/`.
