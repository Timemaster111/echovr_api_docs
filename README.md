# Echo VR Arena API Documentation

Unofficial documentation for Echo VR's HTTP API.

## Summary

Echo VR has an HTTP API available for querying current game state. This API
listens locally on port 6721 (`http://127.0.0.1:6721`). This API now requires a setting to be toggled on.

Note that if any other service is alredy bound to this (TCP) port, which often
happens on Windows, Echo will not be able to bind to it. To kill any services
using it, run `net stop HTTP` in an administrator command prompt.

This repository aims to document all the functionality of this API.

## API Endpoints

Due to more requests for combat data to be shared inside the API, the documentation has been split up into two parts, [Arena](/Arena) and [Combat](/Combat). Most of the data is the same between the two responses, however to make navigation easier some files will exist twice.

### GET /session

In both Combat and Arena.

This returns a detailed representation of the current state of the match. The response is a JSON string, which can be parsed with any standard JSON parser.

### POST /write_camera_mode

Only in Arena

### POST /set_ui_visibility

Only in Arena

### POST /set_enemy_team_muted

Only in Arena

## Concepts

Throughout the API there are a number of concepts that get reused in multiple places. These concepts are documented in this section.

### Vectors

Position, direction, and velocity are represented within the API as an array of [3D vector coordinates in Cartesian space](https://en.wikipedia.org/wiki/Euclidean_vector#In_Cartesian_space). That's a fancy way of saying the array contains three numbers, each representing a distance/speed in either the left-right (`x`), up-down (`y`), or forward-back (`z`) directions. These directions are arranged as `[x, y, z]` in the arrays returned by the API.

Distance is measured in meters, and speed in meters per second. So, for example, a vector coordinate `[0, 1, 0]` could represent either a distance of 1 meter in the "up" direction, or a speed of 1 meter/second in the "up" direction.

For vectors that contain a mix of several directions, you can calculate the total distance or speed (r) using a 3-dimensional version of the [Pythagorean theorem](https://en.wikipedia.org/wiki/Pythagorean_theorem): r<sup>2</sup> = x<sup>2</sup> + y<sup>2</sup> + z<sup>2</sup>

In Echo Arena, distances are measured from the center of the Arena, where the disk spawns (at `[0, 0, 0]`). Positive `z` is in the direction of the orange side of the arena, negative `z` is in the direction of the blue side of the arena. If you're on the blue side of the arena facing the orange team's goal, positive `x` would be towards your left, and negative `x` would be to your right (with left/right reversed for a player on the orange team's side of the arena facing the blue team's side). Positive `y` is "up" (relative to a player's orientation when they spawn) and negative `y` is "down".

So, for example, a player located at [10.0, -5.0, -15.0] would be, from the perspective of someone sitting on the blue team's goal facing the orange team's goal, 10 meters to the left of the center of the arena, on the blue team's side, near the floor.

The Arena is 80m long (counting from orange to blue launch tube exits), 30m wide (counting from the widest point of the side walls) and 20m tall (counting from the tallest part of the arena, in the trenches).

### Session

A "session" is what users typically think of as the "server" you're playing on. When you join a new match, a new session is created, and the session will remain active until all players leave. Sessions IDs are unique, and have no correspondence to the actual, physical or virtual server hardware that's hosting the game.

## Community parts

This section is for community suggestions and common issues

### Requests

Requests list for additions to the API

- position of the local (remote if networked) player(s) exlcuding irl playspace (position of player using boosts and thrusters and not jumps and ducks)
- private games rules set

### Issues

Issues list for the API

### TODO

Things that need doing in the main wiki

- Combat
