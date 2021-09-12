# Write_Camera_Mode

Type: `POST`

Allows setting camera variables.

## Format

`http://127.0.0.1:6721/Write_Camera_Mode/mode={}&&num={}`

### Options

#### `mode={}`

- `pov`
- `level`
- `follow`
- `side`
- `free`
- `api` (no idea what this is)

#### `num={0-9}`

- `0-9` (assumed player number)

### Error cases

- API not enabled
- API user not a spectator
- API user not in a Combat game
