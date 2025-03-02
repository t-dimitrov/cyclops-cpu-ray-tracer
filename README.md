# Cyclops CPU Ray Tracer
This project is a CPU-based ray tracer developed for the purpose of learning and exploring the fundamentals of ray tracing. The implementation follows the book "Ray Tracing in a Weekend" by Peter Shirley, with some additional optimizations and features added.

# Features
- **Core Ray Tracing Implementation**: The core of the project is based on the ray tracing algorithm, in which rays are cast through a 3D scene and their interactions with objects and materials are computed to generate realistic images.
- **Ray-Mesh, Ray-Plane Intersection**: To expand on the basic ray tracing functionality, mesh and plane objects have been added. This ray tracer supports ray-mesh and ray-plane intersection, allowing for the rendering of more complex models beyond the simple geometric primitives. Mesh objects are created from `.obj` files and have a bounding box generated per mesh.
- **Bounding Box Optimization**: In order to optimize the intersection testing process for meshes, a bounding box is dynamically generated around each mesh when the `.obj` model is first loaded. Rays first test against each Mesh's bounding box, which significantly reduces the number of detailed intersection tests needed, improving performance, especially in scenes with a large number of objects.

# Building and Running
## Prerequisites
- C++ Compiler (compatible with C++17 or later)
- CMake (version 3.27 or later)
- Visual Studio (2022 or later)

## Instructions
1. Clone the repository 
```pwsh
git clone https://github.com/t-dimitrov/cyclops-cpu-ray-tracer
```
2. Build the project

If using Visual Studio, open the project by clicking `Open Local Folder`.

If building through cmake call
```pwsh
mkdir build
cd build
cmake ../
```
