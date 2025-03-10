# Asteroids Game

This is a simple implementation of the classic Asteroids game using Python and the Pygame library.

## Features

- Player-controlled spaceship that can rotate and move.
- Shooting mechanics to destroy asteroids.
- Asteroids of varying sizes that split into smaller asteroids when shot.
- Game over condition when the player collides with an asteroid.
- Asteroid field that continuously spawns new asteroids.

## Algorithms

- **Collision Detection:** The game uses simple circle collision detection to determine if the player or a shot collides with an asteroid. This is implemented in the [`collides_with`](circleshape.py) method of the [`CircleShape`](circleshape.py) class.
- **Asteroid Splitting:** When an asteroid is shot, it splits into two smaller asteroids. The new asteroids are given velocities that are rotated slightly from the original asteroid's velocity. This is implemented in the [`split`](asteroid.py) method of the [`Asteroid`](asteroid.py) class.
- **Asteroid Spawning:** Asteroids are spawned at random edges of the screen and given a velocity that directs them towards the center. This is implemented in the [`AsteroidField`](AsteroidField.py) class.

## Programming Paradigm

- **Object-Oriented Programming (OOP):** The game is built using OOP principles. The core game elements (Player, Asteroid, Shot) are represented as classes, inheriting from a base [`CircleShape`](circleshape.py) class. This promotes code reusability and organization.
- **Event-Driven Programming:** The game uses Pygame's event system to handle user input (keyboard presses) and update the game state accordingly.
- **Sprite Groups:** Pygame's sprite groups are used to manage and update the game objects efficiently. The `updatable` group contains all objects that need to be updated each frame, and the `drawable` group contains all objects that need to be drawn.

## File Structure

- `asteroid.py`: Defines the [`Asteroid`](asteroid.py) class.
- `AsteroidField.py`: Defines the [`AsteroidField`](AsteroidField.py) class, which manages the spawning of asteroids.
- `circleshape.py`: Defines the base [`CircleShape`](circleshape.py) class for circular game objects.
- `constants.py`: Defines various game constants such as screen dimensions, asteroid properties, player properties, and shot properties.
- `main.py`: Contains the main game loop and logic.
- `player.py`: Defines the [`Player`](player.py) class.
- `shot.py`: Defines the [`Shot`](shot.py) class.
- `requirements.txt`: Lists the required Python packages.

## How to Run

1.  Install the required packages:

    ```sh
    pip install -r requirements.txt
    ```

2.  Run the game:

    ```sh
    python main.py
    ```

## Controls

- `A`: Rotate left
- `D`: Rotate right
- `W`: Move forward
- `S`: Move backward
- `SPACE`: Shoot

## Credit

I created this project following the Boot.dev Cirriculum
https://github.com/bootdotdev/curriculum
