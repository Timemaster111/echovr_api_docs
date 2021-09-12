# Set_Enemy_Team_Muted

Type: `POST`

Allows automatic muting or unmuting of the enemy team.

## Format

`http://127.0.0.1:6721/set_enemy_team_muted/enabled={true|false}`

### Options

#### `enabled={true|false}`

- `true`
- `false`

### Error cases

- API not enabled
- User is in a transition
- User is in spectator?
