# Echo VR Arena API Documentation

Unofficial documentation for Echo VR's Arena HTTP API.

## Summary

Echo Arena has an HTTP API available for querying current game state. This API
listens locally on port 6721 (`http://127.0.0.1:6721/session`). This API now requires a setting to be toggled on.

Note that if any other service is alredy bound to this (TCP) port, which often
happens on Windows, Echo will not be able to bind to it. To kill any services
using it, run `net stop HTTP` in an administrator command prompt.

This repository aims to document all the functionality of this API.

## API Endpoints

### GET [/session](/Arena/session.md)

This returns a detailed representation of the current state of the match. The response is a JSON string, which can be parsed with any standard JSON parser.

### POST [/write_camera_mode](/Arena/write_camera_mode.md)

Write the camera mode that the current spectator is in, along with the player to focus on.

### POST [/set_ui_visibility](/Arena/set_ui_visibility.md)

Toggle the spectator UI.

### POST [/set_enemy_team_muted](/Arena/set_enemy_team_muted.md)

Set the enemy team to be muted. Unclear who this applies to in spectator currently.

## Arena Concepts

Concepts used in multiple places that only apply to Arena.

### Possession

The API defines "possession" a little more broadly than you might expect (depending on what other sports you may be familiar with that use this term). Not only do players/teams that are currently holding the disk have possession, but teams also maintain possession for 7 seconds after releasing the disk as well, unless the disk is recovered by the opposing team. If the disk is glowing with the color of a specific team, the game considers that team as having "possession".

## Community Parts

Section for things dedicated to the Arena endpoints.

### Issues

- (/session)
- interceptions are not reported correctly

### Quirks

List of things that don't do quite what you expect but still work

- (/session)
- something like team name isn't always orange or blue

### TODO

- (/session)
- packet_loss_ratio stuff
- bumper_shot confirm
- shoulder_pressed values and description
- fill in last throw values
- add in stuff like `[position](#position-1)`
- (general)
- Keep updating
