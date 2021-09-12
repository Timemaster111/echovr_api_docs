# Write_Camera

Type: `POST`

Allows the user to set the camera position, rotation and FOV.

## Format

`http://127.0.0.1:6721/Write_Camera/px=0&&py=1&&pz=2&&qx=0&&qy=0&&qz=0&&qw=1&&fovy=1`

### Options

#### `{px, py, pz}`

Position of the camera. For valid positions see the map dimensions for [Arena](/Arena#ArenaMapPositions).

#### `{qx, qy, qz, qw}`

Rotation of the camera as a quaternion. (/session returns 3 rotation directions).

#### `fovy`

Angle measured from the center of the camera to the top of the camera's frustrum in radians.

### Error cases

- API not enabled
- API user not a spectator
- API user not in an Arena game
