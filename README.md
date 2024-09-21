# Solar System Simulation

## Overview
This project is a simulation of the solar system built using Python's **Turtle** graphics module. It models the gravitational interactions between celestial bodies such as the Sun and planets. The system follows Newtonian physics, where bodies are attracted to each other by gravity.

## Features
- **Simulated Gravity**: Bodies in the system are affected by gravitational forces proportional to their masses.
- **Dynamic Visualization**: The positions of the celestial bodies update in real-time based on their velocities and the forces between them.
- **Expandable**: You can add multiple planets and suns with varying masses and initial velocities.
- **Animated Display**: The simulation uses **Turtle graphics** to visualize the motion of celestial bodies.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Classes](#classes)
- [Future Improvements](#future-improvements)

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/solar-system-simulation.git
    ```
2. Install the required modules (if not already installed):
    ```bash
    pip install turtle
    ```
3. Run the `solar_system_simulation.py` file to start the simulation.

## Usage
- To create a new `SolarSystem` object, provide the screen dimensions (width, height).
- You can add celestial bodies like the Sun or Planets using the respective classes.
- The simulation will update continuously, showing the movement of bodies affected by gravity.


## Classes

### `SolarSystemBody`
Represents a general body in the solar system. It inherits from `turtle.Turtle` and handles properties such as mass, position, velocity, and display size.
- **Attributes**:
  - `mass`: Mass of the body, which influences gravitational force.
  - `position`: Initial coordinates of the body (x, y).
  - `velocity`: The body's velocity vector (vx, vy).
  - `display_size`: Size of the body on the screen, based on its mass.
- **Methods**:
  - `move()`: Updates the body's position based on velocity.
  - `draw()`: Renders the body on the screen as a circle.

### `Sun(SolarSystemBody)`
A subclass of `SolarSystemBody` representing the Sun. Its color is yellow by default.

### `Planet(SolarSystemBody)`
A subclass of `SolarSystemBody` representing a planet. It cycles through a list of colors (red, green, blue) for each new planet.

### `SolarSystem`
Handles the main solar system simulation. It initializes the screen, manages celestial bodies, and updates the simulation.
- **Methods**:
  - `add_body()`: Adds a new body to the solar system.
  - `remove_body()`: Removes an existing body from the solar system.
  - `update_all()`: Updates all celestial bodies' positions and redraws them.
  - `accelerate_due_to_gravity()`: Applies Newtonian gravity to accelerate bodies based on their mass and distance from each other.

## Future Improvements
- **Orbital Paths**: Display the orbital paths of planets.
- **Collision Detection**: Implement detection and handling of collisions between celestial bodies.
- **More Realistic Physics**: Improve the physics engine for more accurate simulations of complex planetary systems.
- **Customizable UI**: Add a user interface to allow on-the-fly adjustments like adding new bodies, changing masses, etc.

## License
This project is licensed under the MIT License.

