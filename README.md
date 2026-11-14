<img width="992" height="561" alt="Univah sdk vs game engines" src="https://github.com/user-attachments/assets/ab724f3c-7a6a-40c3-9a3d-d72b1f520d64" />
<img width="1798" height="1045" alt="hellounivah example" src="https://github.com/user-attachments/assets/2f308f24-2bdb-44be-9a25-6e044757291d" />
<img width="1917" height="1140" alt="Screenshot 2026-11-11 165747" src="https://github.com/user-attachments/assets/7538fd74-9045-4e59-b4dc-1ade23b432c3" />
<img width="972" height="547" alt="Screenshot 2026-11-11 195318" src="https://github.com/user-attachments/assets/b4302fea-db12-4448-b457-97009c53a261" />
<img width="1796" height="1045" alt="Screenshot 2026-11-11 134218" src="https://github.com/user-attachments/assets/058742c1-8286-467f-8871-ad304adf9f91" />

# Univah SDK

The C++ graphics SDK for freelance developers, university researchers and business owners in need of a finished real-time engine inside their commercial application.

You write the program. Univah draws the 3D scene into a window you already own. The public surface is one C++ header, `univah.h`. You link `UnivahSDK.lib` and ship `UnivahEngine.dll` beside your executable. The engine source is not included.

Your client gets your application. The window, menus, and file format stay yours. Univah Pro panels are not required.

**$200 per month** or **$1,327 per year**, per seat.

[Buy the Univah SDK](https://smsoftwarecompany.com)

## Built for graphics programmers

This is a C++ API on a modern OpenGL 4.5 core context. You create the context, make it current, and call `univah::Engine::Create()`. Every later call stays on that thread and draws into the framebuffer you have bound.

A small program is load a model, place it, set the camera, then `Step()` and `Render()` each frame.

```cpp
univah::Engine* engine = univah::Engine::Create(1280, 720, nullptr);
univah::EntityId model = engine->LoadModel("hero.fbx");
engine->SetPosition(model, { 0.f, 0.f, 0.f });
engine->SetCamera({ 0.f, 2.f, 6.f }, { 0.f, 1.f, 0.f });

while (running) {
    engine->Step(frameSeconds);
    engine->Render();
    swap_your_buffers();
}
```
<img width="976" height="546" alt="Univah Film Engine SDK is now available" src="https://github.com/user-attachments/assets/af3f6764-fd1b-4629-a4ba-7a2266dd8f04" />

An artist can also build the shot in Univah Pro and save a .uvh project. 
LoadScene() opens that same file. Pro does not have to be installed on the machine that runs your application.

## What you get
One C++ header and an import library. Your UI toolkit stays yours. The header does not include Qt.
Modern OpenGL 4.5 core rendering on 64-bit Windows 10 and Windows 11.
Model loading, transforms, and cameras with focal length and angle of view.
Directional, point, and spot lights.
Physically based shading, image-based lighting from an HDRI, and ACES tone mapping.
Viewport styles used in production: physically based, sketch, outline, cel, architecture, paint, and wireframe.
Materials and textures, including base color, normal, and glow, plus per-object and global PBR.
Sky, atmosphere, volumetric clouds, and planet clouds.
Simple physics, bend, jiggle, wire, and twist deformers, and 3D text.
Fly-camera and orbit navigation, driven by input from your own window.

<img width="1798" height="1045" alt="hellounivah example" src="https://github.com/user-attachments/assets/e03882f4-e08e-4fac-97e1-f0aa300a1cfe" />
<img width="1570" height="968" alt="exr photoviewer made with univah sdk" src="https://github.com/user-attachments/assets/e89a4da0-0272-4d13-9d16-5f36f6adbf8a" />
<img width="1597" height="1035" alt="univah photo viewer about" src="https://github.com/user-attachments/assets/ae74958f-360a-4953-add2-3e488ed3d732" />

## Two sample programs
Hello Univah and Unicut video Editot, so you can see a finished application built on the same calls.
.uvh scenes saved from Univah Pro load in your program through LoadScene().

## For freelance work
Use the SDK when a client needs a real-time 3D tool and you do not want to spend the contract writing a renderer. You start from a Visual Studio C++ project, keep their interface, and put Univah behind it.

Development access is $200 per month or $1,327 per year for each seat. Applications you ship also follow the royalty schedule included with the SDK. A client receives your application. A client does not receive a license to develop with the Univah SDK.

## Requirements
Windows 10 64-bit, version 1809 or later, or Windows 11
A graphics card that supports OpenGL 4.5
Visual Studio 2022 or newer, with Desktop development with C++
Get the Univah SDK

## Univah SDK, Univah Film Engine, and FiLM ENGINE are trademarks of The Stephanie Michaels Software Company.
