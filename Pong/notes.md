A configuration language is a type of language designed specifically for defining settings, parameters, and options for software, systems, or infrastructure. These languages are used to manage configurations in a structured, human-readable way.

Types of Configuration Languages
Domain-Specific Languages (DSLs)

Designed for a specific purpose (e.g., system setup, application behavior).

Example: JSON, YAML, TOML for app settings.

Declarative Configuration Languages

Define the desired state rather than how to achieve it.

Example: Terraform (HCL), Kubernetes YAML, Ansible Playbooks.

Embedded Scripting Configurations

Some configuration languages allow scripting.

Example: Lua for game settings, Nginx configuration

---

**LUA**
Lua is a lightweight, high-performance scripting language designed for embedded systems, game development, and other applications where efficiency is crucial. It was created in Brazil in the early 1990s and is known for its simplicity, flexibility, and ease of integration with other languages, especially C and C++.
Where is Lua Used?
Game Development: Popular in engines like Unity (via plugins), Roblox, and LOVE2D.

Embedded Systems: Used in IoT, firmware, and networking applications.

Scripting: Found in apps like Adobe Lightroom and World of Warcraft.

Automation: Used for customizing software behavior in various industries.

---

Love2D
LÖVE (Love2D) is a free, open-source game framework for making 2D games using Lua. It is lightweight, easy to use, and cross-platform, making it popular among indie developers and hobbyists.

🔹 Key Features
Uses Lua: Simple and fast scripting.

Cross-Platform: Runs on Windows, macOS, Linux, Android, and iOS.

Hardware-Accelerated: Uses OpenGL for rendering.

Physics Engine: Integrated Box2D for physics.

Audio & Input Handling: Supports sound, music, keyboard, mouse, and gamepad input.

Love.load()
-used for iniitializing our game state at the very beginnig of program execution

Love.update(dt)
-called each frame by Love:
dt will be the elapse time in seconds since the last frame and we can use this to scale any changes in our game for even behaviour across frame rates

love.draw()
-called each frame by Love after update for drawing things to the screen once they've changed.
LOVE2D expects these functions to be implemented in main.lua and calls them internally ;if we don't define the them,it will still function but our game will fundamentally incomplete at least uf update or draw are missing!

Love.graphics.printf(text,x,y,[width],[align])
-versatile print function that can align text left,right,or center on the screen
love.window.setMode(width,height,params)
-used to initialize the window's dimension and to set parameters like vsync (vertical sync),whether we're fullscreen or not whether he window is resizable after startup.won't be using past this example in favour of the push virtual resolution library.which has ots own method like this but useful to know if encountered in other code

---

`Game Loop`

Process Input->Update Game State->Draw Frame->Repeat

---

`Scope of this game`
Draw Shapes to the screen
Control 2D position of the paddles based on input
Collision detection between the paddles and the ball to deflect ball back toward opponent
Collision Detection between ball and map boundaries to keep ball within vertical bounds and to detect score(outside horizontal bounds)
Sound effects when ball hits paddles/walls or when a point is scored for flavor
Scorekeeping to determine winner
