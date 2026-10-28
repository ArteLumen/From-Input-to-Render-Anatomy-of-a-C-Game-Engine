# From-Input-to-Render-Anatomy-of-a-C-Game-Engine
🎮 Minimal C Game Engine CoreA lightweight, performance-focused game engine architecture written in C. This project demonstrates the core concepts of low-level game development, including custom data structures, modular pipeline phases, and a classic Game Loop.📌 FeaturesCustom Game Loop: Synchronized execution of input, update, and rendering phases.Entity Data Structures: Lightweight C structs for memory-efficient game entities.Modular Architecture: Clean separation of input processing, game logic, and scene rendering.Zero External Dependencies: Standard C library execution for maximum portability.🚀 Getting StartedPrerequisitesYou need a C compiler installed on your system:GCC (Linux / MinGW on Windows)Clang (macOS / Linux)MSVC (Windows Visual Studio)Compilation & ExecutionOn Linux / macOS:Bash# Compile the source code
gcc -o game_engine main.c

# Run the executable
./game_engine
On Windows (CMD / PowerShell):DOS:: Compile using GCC
gcc -o game_engine.exe main.c

:: Run the executable
game_engine.exe
🕹️ ControlsKeyActionwMove the player character forwardqQuit the engine loop and shutdown🛠️ Engine Architecture Overview [ Start ]
    │
    ▼
[ Initialize Player / Entities ]
    │
    ▼
┌───► [ 1. Process Input ] ──── ( 'q' pressed? ──► Exit )
│            │
│            ▼
│     [ 2. Update Logic ] ( Physics & Transformations )
│            │
│            ▼
└──── [ 3. Render Frame  ] ( Draw Scene )
🔮 Future Improvements[ ] Add 2D rendering support using SDL2 or Raylib.[ ] Implement delta time ($\Delta t$) for frame-rate-independent physics.[ ] Expand entity management with a simple Component system.📜 LicenseThis project is open-source and available under the APACHE 2.0 License.
