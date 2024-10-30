# Not So Grand 7 (NSG 7)

Welcome to Not So Grand 7, an open-world action-adventure game inspired by the classic GTA series. This README will guide you through setting up and developing NSG 7 using Unreal Engine and Visual Studio Code.

## Table of Contents

- [Game Overview](#game-overview)
- [Prerequisites](#prerequisites)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Creating the Project](#creating-the-project)
- [Basic Game Structure](#basic-game-structure)
- [Developing Game Features](#developing-game-features)
- [Building and Testing](#building-and-testing)
- [Resources](#resources)

## Game Overview

Not So Grand 7 is set in a fictional city where players can explore, complete missions, and interact with a diverse cast of characters. The game features:

- Open-world exploration
- Engaging storylines and side missions
- Varied gameplay mechanics including driving and combat

## Prerequisites

Before you start, ensure you have the following installed:

- [Unreal Engine 5](https://www.unrealengine.com/en-US/download)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Visual Studio 2019/2022](https://visualstudio.microsoft.com/) (with C++ components)
- Basic understanding of C++ and game design principles

## Setting Up the Development Environment

1. **Install Unreal Engine**:
   - Download and install Unreal Engine from the Epic Games Launcher.

2. **Install Visual Studio Code**:
   - Download and install Visual Studio Code from its official site.

3. **Install Visual Studio**:
   - Download Visual Studio and ensure you install the "Game Development with C++" workload.

4. **Set Up C++ Development**:
   - Open Unreal Engine and create a new project. Choose a "Games" template and select "Blank" with C++ support.

## Creating the Project

1. **Launch Unreal Engine**.
2. **Create a New Project**:
   - Select "Games" > "Next".
   - Choose "Blank" and make sure to enable C++ support.
   - Name your project "NotSoGrand7" and choose a location.
   - Click "Create".

3. **Open the Project in VSCode**:
   - Navigate to your project folder and open it in VSCode for coding.

## Basic Game Structure

### Setting Up Game Modules

1. **Create Main Game Files**:
   - In the `Source/NotSoGrand7/` folder, create the following files:
     - `NSGGameMode.h`
     - `NSGGameMode.cpp`
     - `NSGCharacter.h`
     - `NSGCharacter.cpp`

2. **Game Mode**:
   - Define your game mode in `NSGGameMode.h`:
     ```cpp
     #pragma once
     #include "CoreMinimal.h"
     #include "GameFramework/GameModeBase.h"
     #include "NSGGameMode.generated.h"

     UCLASS()
     class NOTSOGRAND7_API ANSGGameMode : public AGameModeBase
     {
         GENERATED_BODY()

     public:
         ANSGGameMode();
     };
     ```
   - Implement in `NSGGameMode.cpp`:
     ```cpp
     #include "NSGGameMode.h"

     ANSGGameMode::ANSGGameMode()
     {
         // Set default pawn class to our character
         DefaultPawnClass = ANSGCharacter::StaticClass();
     }
     ```

3. **Player Character**:
   - Define your player character in `NSGCharacter.h`:
     ```cpp
     #pragma once
     #include "CoreMinimal.h"
     #include "GameFramework/Character.h"
     #include "NSGCharacter.generated.h"

     UCLASS()
     class NOTSOGRAND7_API ANSGCharacter : public ACharacter
     {
         GENERATED_BODY()

     public:
         ANSGCharacter();
     };
     ```
   - Implement in `NSGCharacter.cpp`:
     ```cpp
     #include "NSGCharacter.h"

     ANSGCharacter::ANSGCharacter()
     {
         // Set default values for character properties
     }
     ```

## Developing Game Features

### Adding Driving Mechanics

1. **Create a Vehicle Class**:
   - Add `NSGVehicle.h` and `NSGVehicle.cpp` similar to the character setup.

2. **Implement Driving Logic**:
   - Use Unreal Engine's vehicle classes to implement handling and physics.

### Creating the Game World

1. **Design the Map**:
   - Use the Unreal Engine editor to create a city layout with buildings, roads, and NPCs.

2. **Add Missions**:
   - Create mission systems that players can interact with.

## Building and Testing

1. **Build the Project**:
   - Use the Unreal Engine editor to build the project for the first time.
   
2. **Test in Editor**:
   - Click "Play" in the editor to test your game.

3. **Debugging**:
   - Use Visual Studio to set breakpoints and debug your C++ code.

## Resources

- [Unreal Engine Documentation](https://docs.unrealengine.com/)
- [Unreal Engine C++ Programming](https://www.unrealengine.com/en-US/onlinelearning-courses/c-introduction)
- [Community Forums](https://forums.unrealengine.com/)

## Contributing

Feel free to fork the project and submit pull requests for new features, improvements, or fixes.

## License

This project is licensed under the MIT License.
