# Session

Type: `GET`

This returns a detailed representation of the current state of the match. The response is a JSON string, which can be parsed with any standard JSON parser.

Example response (formatted for readability):

<pre>
{
    <a href="#client_name">"client_name"</a>: "Timemaster111",
    <a href="#sessionid">"sessionid"</a>: "1C32B3DA-F1F6-4B17-8BAE-FD1BC59C28BD",
    <a href="#sessionip">"sessionip"</a>: "184.154.39.222",
    <a href="#match_type">"match_type"</a>: "Echo_Combat" // "Echo_Combat", "Echo_Combat_Private", "Social_2.0", "INVALID GAMETYPE"
    <a href="#map_name">"map_name"</a>: "mpl_lobby_b2" // "mpl_lobby_b2", mpl_combat_dyson, mpl_combat_combustion, mpl_combat_fission, mpl_combat_gauss, "INVALID LEVEL"
    <a href="#game_clock">"game_clock"</a>: 215.09978,
    <a href="#game_clock_display">"game_clock_display"</a>: "03:35.09",
    <a href="#private_match">"private_match"</a>: false,
    <a href="#total_round_count">"total_round_count"</a>: 1,
    <a href="#blue_round_score">"blue_round_score"</a>: 0,
    <a href="#orange_round_score">"orange_round_score"</a>: 0,
    <a href="#blue_points">"blue_points"</a>: 2,
    <a href="#orange_points">"orange_points"</a>: 4,
    <a href="#tournament_match">"tournament_match"</a>: false,
    <a href="#blue_team_restart_request">"blue_team_restart_request"</a>: 0,
    <a href="#orange_team_restart_request">"orange_team_restart_request"</a>: 0,
    <a href="#right_shoulder_pressed">"right_shoulder_pressed"</a>: 0.0,
    <a href="#right_shoulder_pressed2">"right_shoulder_pressed2"</a>: 0.0,
    <a href="#left_shoulder_pressed">"left_shoulder_pressed"</a>: 0.0,
    <a href="#left_shoulder_pressed2">"left_shoulder_pressed2"</a>: 0.0,
    <a href="#packet_loss_ratio">"packet_loss_ratio"</a>: TBC,
    <a href="#game_status">"game_status"</a>: "score", // "pre_match", "round_start", "playing", "score", "round_over", "round_start", "post_match", "pre_sudden_death", "sudden_death", "post_sudden_death"
    <a href="#pause">"pause"</a>: {
        <a href="#pausepaused_state">"paused_state"</a>: "unpaused", // "unpaused", "unpausing", "paused", "paused_requested"
        <a href="#pauseunpaused_team">"unpaused_team"</a>: "none", // "orange", "blue", "none"
        <a href="#pausepaused_requested_team">"paused_requested_team"</a>: "none", // "orange", "blue", "none"
        <a href="#pauseunpaused_timer">"unpaused_timer"</a>: 0.0,
        <a href="#pausepaused_timer">"paused_timer"</a>: 0.0
    },
    <a href="#player">"player"</a>: {
        <a href="#playervr_left">"vr_left"</a>: [
            0.78700006,
            0.072000004,
            0.61300004
        ],
        <a href="#playervr_position">"vr_position"</a>: [
            -3.9650002,
            2.2310002,
            -34.506001
        ],
        <a href="#playervr_forward">"vr_forward"</a>: [
            -0.61700004,
            0.091000006,
            0.78200006
        ],
        <a href="#playervr_up">"vr_up"</a>: [
            0.0,
            0.99300003,
            -0.116
        ]
    },
    <a href="#teams">"teams"</a>: [
        {
            <a href="#teamsteam">"team"</a>: "BLUE TEAM",
            <a href="#teamspossession">"possession"</a>: false,
            <a href="#teamsstats">"stats"</a>: {
            },
            <a href="#teamsplayers">"players"</a>: [
                {
                    <a href="#teamsplayersname">"name"</a>: "Timemaster111",
                    <a href="#teamsplayersplayerid">"playerid"</a>: 0,
                    <a href="#teamsplayersuserid">"userid"</a>: 3561909181390317,
                    <a href="#teamsplayersnumber">"number"</a>: 5,
                    <a href="#teamsplayerslevel">"level"</a>: 50,
                    <a href="#teamsplayersping">"ping"</a>: 48,
                    <a href="#teamsplayersstunned">"stunned"</a>: false,
                    <a href="#teamsplayersinvulnerable">"invulnerable"</a>: false,
                    <a href="#teamsplayersholding_left">"holding_left"</a>: "none",
                    <a href="#teamsplayersholding_right">"holding_right"</a>: "none",
                    <a href="#teamsplayersweapon">"weapon"</a>: "Pulsar",
                    <a href="#teamsplayersarm">"arm"</a>: "right",
                    <a href="#teamsplayerstacmod">"tacmod"</a>: "none",
                    <a href="#teamsplayersordnance">"ordnance"</a>: "none",
                    <a href="#teamsplayersstats">"stats"</a>: {
                    },
                    <a href="#teamsplayersvelocity">"velocity"</a>: [
                        0.48200002,
                        0.83300006,
                        -2.3240001
                    ],
                    <a href="#teamsplayershead">"head"</a>: {
                        <a href="#teamsplayersheadposition">"position"</a>: [
                            -2.1360002,
                            2.098,
                            -33.876003
                        ],
                        <a href="#teamsplayersheadforward">"forward"</a>: [
                            0.14600001,
                            -0.36400002,
                            0.92000002
                        ],
                        <a href="#teamsplayersheadleft">"left"</a>: [
                            0.98400003,
                            -0.045000002,
                            -0.17400001
                        ],
                        <a href="#teamsplayersheadup">"up"</a>: [
                            0.105,
                            0.93000007,
                            0.35200003
                        ]
                    },
                    <a href="#teamsplayersbody">"body"</a>: {
                        <a href="#teamsplayersbodyposition">"position"</a>: [
                            -2.1360002,
                            2.098,
                            -33.876003
                        ],
                        <a href="#teamsplayersbodyforward">"forward"</a>: [
                            0.296,
                            0.001,
                            0.95500004
                        ],
                        <a href="#teamsplayersbodyleft">"left"</a>: [
                            0.95500004,
                            -0.0020000001,
                            -0.296
                        ],
                        <a href="#teamsplayersbodyup">"up"</a>: [
                            0.001,
                            1.0,
                            -0.001
                        ]
                    },
                    <a href="#teamsplayersrhand">"rhand"</a>: {
                        <a href="#teamsplayersrhandpos">"pos"</a>: [
                            -2.3390002,
                            1.8030001,
                            -33.733002
                        ],
                        <a href="#teamsplayersrhandforward">"forward"</a>: [
                            -0.259,
                            0.74000001,
                            0.62
                        ],
                        <a href="#teamsplayersrhandleft">"left"</a>: [
                            0.80900002,
                            -0.18400002,
                            0.55800003
                        ],
                        <a href="#teamsplayersrhandup">"up"</a>: [
                            0.52700001,
                            0.64700001,
                            -0.55200005
                        ]
                    },
                    <a href="#teamsplayerslhand">"lhand"</a>: {
                        <a href="#teamsplayerslhandpos">"pos":</a> [
                            -2.0700002,
                            1.8610001,
                            -33.788002
                        ],
                        <a href="#teamsplayerslhandforward">"forward"</a>: [
                            -0.44800001,
                            0.73100001,
                            0.51500005
                        ],
                        <a href="#teamsplayerslhandleft">"left"</a>: [
                            0.89200002,
                            0.32200003,
                            0.317
                        ],
                        <a href="#teamsplayerslhandup">"up"</a>: [
                            0.066,
                            0.60100001,
                            -0.79600006
                        ]
                    },
                },
                {
                /* ... more players ... */
                }
            ]
        },
        {
            <a href="#teams">"team"</a>: "ORANGE TEAM",
            /* ... same as blue team ... */
        },
        {
            <a href="#teams">"team"</a>: "SPECTATORS",
            /* ... same as blue team ... */
        }
    ]
}  
</pre>

#### Properties

The response is a JSON object, with the following properties:

#### `client_name`

The username of the signed-in user.

#### `sessionid`

A 128-bit string-encoded GUID of the session.

#### `sessionip`

IP address to the current server

#### `match_type`

Represents the type of match being played.

Possible values:

- `"Echo_Combat"`
- `"Echo_Combat_Private"`
- `"Social_2.0"`
- `"INVALID GAMETYPE"`

#### `map_name`

Name of the map being played.

Possible values:

- `"mpl_lobby_b2"` - Lobby
- `mpl_combat_dyson` - Combat maps
- `mpl_combat_combustion`
- `mpl_combat_fission`
- `mpl_combat_gauss`
- `"INVALID LEVEL"`

#### `game_clock`

Current game time in seconds.

#### `game_clock_display`

Current game time as shown in game.

#### `private_match`

Whether the current session is a private lobby.

#### `total_round_count`

Total number of rounds to be played in the match.

#### `blue_round_score`

Total number of rounds that blue has won.

#### `orange_round_score`

Total number of rounds that orange has won.

#### `blue_points`

Number of points blue has scored this round.

#### `orange_points`

Number of points orange has scored this round.

#### `tournament_match`

Whether the current session is being used for an official tournament orchestrated in collaboration with the Echo Arena developers. This is [for possible future integration with ESL and other organized tournaments](https://discordapp.com/channels/326412222119149578/506931756675497986/510566303367430145).

#### `blue_team_restart_request`

Whether or not the blue team is requesting a restart.

#### `orange_team_restart_request`

Whether or not the orange team is requesting a restart.

#### `right_shoulder_pressed`

Touch controller input

#### `right_shoulder_pressed2`

Touch controller input

#### `left_shoulder_pressed`

Touch controller input

#### `left_shoulder_pressed2`

Touch controller input

#### `packet_loss_ratio`

Number of packets missed bu the client out of the total number of packets sent by the server in a 5 second window.

#### `game_status`

The current game's status.

Possible values:

- `"pre_match"`
- `"round_start"`
- `"playing"`
- `"score"`
- `"round_over"`
- `"round_start"`
- `"post_match"`
- `"pre_sudden_death"`
- `"sudden_death"`
- `"post_sudden_death"`

#### `pause`

Details about whether the game is currently paused.

#### `pause.paused_state`

Current pause state of the match.

Possible values:

- `"unpaused"`
- `"unpausing"`
- `"paused"`
- `"paused_requested"`

#### `pause.unpaused_team`

Team that unpaused the game.

Possible values:

- `"orange"`
- `"blue"`
- `"none"`

#### `pause.paused_requested_team`

Team that pressed the pause button.

Possible values:

- `"orange"`
- `"blue"`
- `"none"`

#### `pause.unpaused_timer`

Time until gameplay will resume.

#### `pause.paused_timer`

Time since game was paused.

#### `player`

An object representing the current state of the local VR player. This is used for positions of the player within their playspace.

#### `player.vr_left`

The direction that the left side of the player's head is facing within their playspace.

#### `player.vr_position`

An array representing the player's position within their playspace.

#### `player.vr_forward`

The direction that the player's head is facing within their playspace.

#### `player.vr_up`

The direction that the top side of the player's head is facing within their playspace.

#### `teams`

An array of objects containing data used to instantiate the game's two teams. The first element in the array is always the blue team, while the second is always the orange team and the third is always the spectators.

#### `teams[].team`

A human-readable team name. Usually either "ORANGE TEAM" or "BLUE TEAM", but if all the players on a team have the same team name (set by pressing F11 while in a match or the lobby) it will be that instead.

#### `teams[].stats`

An object containing data used to instantiate the team's current stats.

#### `teams[].players`

An array of objects containing data used to instantiate the team's players.

#### `teams[].players[].name`

The username of the player.

#### `teams[].players[].playerid`

A number representing ID of the player within the current game session.

#### `teams[].players[].userid`

A unique number identifying the player across all game sessions.

#### `teams[].players[].number`

The number a player chose for themselves in the customization room.

Need to verify how this works in the new update.

#### `teams[].players[].level`

A number (1-50) representing the player's experience "level". New accounts start as level 1, and will usually reach level 50 after a few hundred games in public matchmaking.

Note that there a rare bug where this number may be 0 in the UI in some cases; it's possible this bug may also affect the API (though this has yet to be verified).

#### `teams[].players[].ping`

Current ping (network latency to server) of this player.

#### `teams[].players[].stunned`

Whether the player is currently stunned.

#### `teams[].players[].invulnerable`

Whether or not the player is currently immune to stuns. Players will be in this state for 3 seconds after they are stunned.

#### `teams[].players[].holding_left`

The item or object the player is holding in their left hand.

Possible values:

- `"disc"`
- player id (`"0"`, `"1"`)
- `"geo"`

#### `teams[].players[].holding_right`

The item or object the player is holding in their right hand.

Possible values:

- player id (`"0"`, `"1"`)
- `"geo"`

#### `teams[].players[].holding_right`

The item or object the player is holding in their right hand.

Possible values:

- player id (`"0"`, `"1"`)
- `"geo"`

#### `teams[].players[].weapon`

The weapon the player has selected.

Possible values:

- pulsar
- idk i don't play combat i'll add the rest

#### `teams[].players[].arm`

The arm the user is currently holding their gun in.

Possible values:

- `Left`
- `Right`
- `None`

#### `teams[].players[].tacmod`

The TacMod the player has selected.

Possible values:

- ok really I have no clue

#### `teams[].players[].ordnance`

The Ordnance the player has selected

Possible values:

- not an inkling

#### `teams[].players[].stats`

An object containing data used to instantiate the player's current stats. See [`teams[].stats`](#teamsstats) for a list of available stats.

#### `teams[].players[].velocity`

The current velocity (speed and direction of movement) of the player.

#### `teams[].players[].head`

An object containing position and rotation of the head of the player

#### `teams[].players[].head.position`

The position of the player's head in the map.

#### `teams[].players[].head.forward`

The direction that the player's head is facing.

#### `teams[].players[].head.left`

The direction that the left side of the player's head is facing.

#### `teams[].players[].head.up`

The direction that the top side of the player's head is facing.

#### `teams[].players[].body`

An object containing position and rotation of the body of the player

#### `teams[].players[].body.position`

The position of the player's body in the map.

#### `teams[].players[].body.forward`

The direction that the player's body is facing.

#### `teams[].players[].body.left`

The direction that the left side of the player's body is facing.

#### `teams[].players[].body.up`

The direction that the top side of the player's body is facing.

#### `teams[].players[].rhand`

An object containing position and rotation data for the right hand.

#### `teams[].players[].rhand.pos`

The position of the player's right hand within the map.

#### `teams[].players[].rhand.forward`

The direction that the player's right hand is facing.

#### `teams[].players[].rhand.left`

The direction that the left side of the player's right hand is facing.

#### `teams[].players[].rhand.up`

The direction that the top side of the player's right hand is facing.

#### `teams[].players[].lhand`

An object containing position and rotation data for the left hand.

#### `teams[].players[].lhand.pos`

The position of the player's left hand within the map.

#### `teams[].players[].lhand.forward`

The direction that the player's left hand is facing.

#### `teams[].players[].lhand.left`

The direction that the left side of the player's left hand is facing.

#### `teams[].players[].lhand.up`

The direction that the top side of the player's left hand is facing.
