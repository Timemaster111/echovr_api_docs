# Echo VR Combat API Documentation

Unofficial documentation for Echo VR's Combat HTTP API.

## Summary

Echo Combat has an HTTP API available for querying current game state. This API
listens locally on port 6721 (`http://127.0.0.1:6721`). This API now requires a setting to be toggled on.

Note that if any other service is alredy bound to this (TCP) port, which often
happens on Windows, Echo will not be able to bind to it. To kill any services
using it, run `net stop HTTP` in an administrator command prompt.

This repository aims to document all the functionality of this API.

## API Endpoints

### GET [/session](/Combat/session.md)

This returns a detailed representation of the current state of the match. The response is a JSON string, which can be parsed with any standard JSON parser.

### POST [/write_camera](/Combat/write_camera.md)

Write the camera position, rotation and FOV for the current spectator.

### POST [/write_camera_mode](/Combat/write_camera_mode.md)

Write the camera mode that the current spectator is in, along with the player to focus on.

### POST [/set_ui_visibility](/Combat/set_ui_visibility.md)

Toggle the player HUD.

### POST [/set_enemy_team_muted](/Combat/set_enemy_team_muted.md)

Set the enemy team to be muted. Unclear who this applies to in spectator currently.

## Combat Concepts

Concepts used in multiple places that only apply to Combat.

### Combat Map Positions

The following is data taken about where things are in the Combat maps. For the write camera endpoint this is what you need to position the camera inside or around, and for players this is the limits of where they can go.

## Community Parts

Section for things dedicated to the Combat endpoints.

### Issues

- (/session)

### Quirks

List of things that don't do quite what you expect but still work

- (/session)
- something like team name isn't always orange or blue

### TODO

- (/session)
- packet_loss_ratio stuff
- shoulder_pressed values and description
- add in stuff like `[position](#position-1)`
- (general)
- Keep updating
