---
layout: default
title: Parameter Reference
parent: Smart GameObjects
nav_order: 4
has_children: false
---

# Parameter Reference:

You can use this table to look up IDs of actions and/or paramters if manually creating conditions/actions during runtime or via other scripts.

### Smart Actions:

| Index | Value |
| ----- | ----- |
| 0 | Do Nothing... |
| 1 | Tween / Translate / Start Translation |
| 2 | Tween / Translate / Stop Translation |
| 3 | Tween / Translate / Pause Translation |
| 4 | Tween / Translate / Resume Translation |
| 5 | Tween / Translate / Start Path Translation |
| 6 | Tween / Translate / Stop Path Translation |
| 7 | Tween / Translate / Set Translation Target |
| 8 | Tween / Translate / Set Translation Target To Focus Target |
| 9 | Tween / Translate / Set Translation Target To Last Raycast Hit |
| 10 | Tween / Rotate / Look At Focus Target |
| 11 | Tween / Rotate / Look At Main Camera |
| 12 | Tween / Rotate / Stop Look At |
| 13 | Tween / Rotate / Start Rotating |
| 14 | Tween / Rotate / Stop Rotating |
| 15 | Tween / Rotate / Pause Rotation |
| 16 | Tween / Rotate / Resume Rotation |
| 17 | Tween / Rotate / Set Rotation Target |
| 18 | Tween / Rotate / Set Rotation Target To Focus Target |
| 19 | Tween / Rotate / Set Rotation Target To Last Raycast Hit Normal |
| 20 | Tween / Scale / Start Scale |
| 21 | Tween / Scale / Stop Scale |
| 22 | Tween / Scale / Pause Scale |
| 23 | Tween / Scale / Resume Scale |
| 24 | Tween / Scale / Set Scale Target |
| 25 | Tween / Scale / Set Scale Target To Focus Target Scale |
| 26 | Transform / Parent To Focus Target |
| 27 | Transform / Clear Parent |
| 28 | Transform / Set To Initial Values |
| 29 | Transform / Clear Transform Values |
| 30 | Transform / Set To Focus Target Values |
| 31 | Raycast / Raycast Single |
| 32 | Raycast / Raycast All |
| 33 | Raycast / Raycast Row |
| 34 | Raycast / Circle Cast (experimental) |
| 35 | Raycast / Grid Cast |
| 36 | Raycast / Scatter Cast |
| 37 | Raycast / Fan Cast |
| 38 | Raycast / Sphere Cast |
| 39 | Raycast / Sphere Cast All |
| 40 | Raycast / Box Cast |
| 41 | Raycast / Box Cast All |
| 42 | Raycast / Capsule Cast |
| 43 | Raycast / Line Cast |
| 44 | Animator / Set Trigger |
| 45 | Animator / Play |
| 46 | Animator / Stop Playback |
| 47 | Spawn / At Focus Target |
| 48 | Spawn / At Last Raycast Hit |
| 49 | Spawn / At All Raycast Hits |
| 50 | Spawn / At All Colliders |
| 51 | Spawn / At Last Collision (trigger detection) |
| 52 | Spawn / At Last Collider |
| 53 | Spawn / At All Target Positions |
| 54 | Spawn / At This Position |
| 55 | NavMeshAgent / Follow Focus Target |
| 56 | NavMeshAgent / Flee From Focus Target |
| 57 | NavMeshAgent / Follow Focus Target Path |
| 58 | NavMeshAgent / Follow Own Path |
| 59 | NavMeshAgent / Wander |
| 60 | Targets / Target Last Collision (trigger detection) |
| 61 | Targets / Target Last Collider Contact |
| 62 | Targets / Target All Colliders Contacts |
| 63 | Targets / Target All Raycast Hits |
| 64 | Targets / Target Collider Contacts With Tag |
| 65 | Targets / Target Raycast Hits With Tag |
| 66 | Targets / Clear All |
| 67 | Focus / On Nothing |
| 68 | Focus / On First Target |
| 69 | Focus / On Last Target |
| 70 | Focus / On Farthest Target |
| 71 | Focus / On Nearest Target |
| 72 | Focus / On Target With Tag |
| 73 | Focus / On Farthest Target With Tag |
| 74 | Focus / On Nearest Target With Tag |
| 75 | Targets / Clear Nearest Target |
| 76 | Targets / Clear Farthest Target |
| 77 | GameObject / Deactivate |
| 78 | GameObject / Destroy |
| 79 | Debug / Log Info Message |
| 80 | Debug / Log Warning Message |
| 81 | Debug / Log Error Message |
| 82 | Debug / Root Direction |
| 83 | Debug / Float Message |
| 84 | Debug / Boolean Message |
| 85 | Rigidbody / Seek Focus Target |
| 86 | Rigidbody / Richochet |
| 87 | Rigidbody / Add Force |
| 88 | Rigidbody / Add Impulse Force |
| 89 | Rigidbody / Add Acceleration Force |
| 90 | Rigidbody / Change Velocity |
| 91 | Rigidbody / Add Torque Force |
| 92 | Rigidbody / Add Torque Impulse Force |
| 93 | Rigidbody / Add Torque Acceleration Force |
| 94 | Rigidbody / Add Relative Force |
| 95 | Rigidbody / Add Relative Torque |
| 96 | Tween / Translate / Set Curve |
| 97 | Tween / Rotate / Set Curve |
| 98 | Tween / Scale / Set Curve |
| 99 | Tween / Translate / Set Path Curve |
| 100 | Smart GameObject / Disable Behavior |
| 101 | Smart GameObject / Enable Behavior |
| 102 | Smart GameObject / Force Stop Behavior Delay |
| 103 | Smart GameObject / Stop All Coroutines |
| 104 | Smart GameObject / Disable Self |
| 105 | Transform / Set Position / To Custom Value |
| 106 | Transform / Set Rotation / To Custom Value |
| 107 | Transform / Set Scale / To Custom Value |
| 108 | Transform / Set Position / To Focus Target Position |
| 109 | Transform / Set Rotation / To Focus Target Rotation |
| 110 | Transform / Set Scale / To Focus Target Scale |
| 111 | Targets / Remove Focus Target |
| 112 | Targets / Remove Null Entries |
| 113 | Targets / Reverse Order |
| 114 | Focus / On Last Spawned |
| 115 | Rigidbody / Add Forward Force |
| 116 | Raycast / Clear Hits |
| 117 | Rigidbody / Clear Contacts |
| 118 | Transform / Look At / Last Spawn |
| 119 | Transform / Look At / Last Collider Contact |
| 120 | Transform / Look At / Last Raycast Hit |
| 121 | Transform / Look At / Last Collision Contact (trigger detection) |
| 122 | Transform / Look At / Focus Target's Last Spawn |
| 123 | Transform / Look At / Focus Target |

### Float parameters:

| Index | Value |
| ----- | ----- |
| 0 | Custom Value (read-only) /  |
| 1 | Smart Variable |
| 2 | Constants (read-only) /  |
| 3 | Constants (read-only) /  |
| 4 | Constants (read-only) /  |
| 5 | Constants (read-only) /  |
| 6 | Constants (read-only) /  |
| 7 | Constants (read-only) /  |
| 8 | Constants (read-only) /  |
| 9 | Constants (read-only) /  |
| 10 | Transform / Position / X (Global) |
| 11 | Transform / Position / Y (Global) |
| 12 | Transform / Position / Z (Global) |
| 13 | Transform / Position / X (Local) |
| 14 | Transform / Position / Y (Local) |
| 15 | Transform / Position / Z (Local) |
| 16 | Transform / Rotation / X (Global) |
| 17 | Transform / Rotation / Y (Global) |
| 18 | Transform / Rotation / Z (Global) |
| 19 | Transform / Rotation / X (Local) |
| 20 | Transform / Rotation / Y (Local) |
| 21 | Transform / Rotation / Z (Local) |
| 22 | Transform / Scale / X (Global) (read-only) /  |
| 23 | Transform / Scale / Y (Global) (read-only) /  |
| 24 | Transform / Scale / Z (Global) (read-only) /  |
| 25 | Transform / Scale / X (Local) |
| 26 | Transform / Scale / Y (Local) |
| 27 | Transform / Scale / Z (Local) |
| 28 | Transform / Child Count (read-only) /  |
| 29 | Rigidbody / Angular Velocity Magnitude (read-only) /  |
| 30 | Rigidbody / Max Angular Velocity |
| 31 | Rigidbody / Mass |
| 32 | Rigidbody / Drag |
| 33 | Rigidbody / Angular Drag |
| 34 | Rigidbody / Max Depenetration Velocity |
| 35 | Rigidbody / Velocity Magnitude (read-only) /  |
| 36 | NavMeshAgent / Acceleration |
| 37 | NavMeshAgent / Angular Speed |
| 38 | NavMeshAgent / Base Offset |
| 39 | NavMeshAgent / Velocity Magnitude (read-only) /  |
| 40 | NavMeshAgent / Speed |
| 41 | NavMeshAgent / Height |
| 42 | NavMeshAgent / Radius |
| 43 | NavMeshAgent / Stopping Distance |
| 44 | AudioSource / Doppler Level |
| 45 | AudioSource / Min Distance |
| 46 | AudioSource / Max Distance |
| 47 | AudioSource / Volume |
| 48 | AudioSource / Pan Stereo |
| 49 | AudioSource / Pitch |
| 50 | AudioSource / Reverb Zone Mix |
| 51 | AudioSource / Spread |
| 52 | AudioSource / Spatial Blend |
| 53 | AudioSource / Time |
| 54 | Animator / Float Parameter |
| 55 | Animator / Integer Parameter |
| 56 | Animator / Speed |
| 57 | Animator / Pivot Weight (read-only) /  |
| 58 | Animator / Playback Time |
| 59 | Animator / Left Feet Bottom Height (read-only) /  |
| 60 | Animator / Right Feet Bottom Height (read-only) /  |
| 61 | Animator / Angular Velocity Magnitude (read-only) /  |
| 62 | Distance (read-only) /  |
| 63 | Distance (read-only) /  |
| 64 | Distance (read-only) /  |
| 65 | Distance (read-only) /  |
| 66 | Distance (read-only) /  |
| 67 | Distance (read-only) /  |
| 68 | Distance (read-only) /  |
| 69 | Distance (read-only) /  |
| 70 | Distance (read-only) /  |
| 71 | Distance (read-only) /  |
| 72 | Distance (read-only) /  |
| 73 | Distance (read-only) /  |
| 74 | Time (read-only) /  |
| 75 | Time (read-only) /  |
| 76 | Time (read-only) /  |
| 77 | Time (read-only) /  |
| 78 | Time (read-only) /  |
| 79 | Physics / Max Ray Distance |
| 80 | Physics / Ray Spacing |
| 81 | Physics / Ray Count |
| 82 | Physics / Ray Vertical Scatter |
| 83 | Physics / Ray Horizontal Scatter |
| 84 | Physics / Max Collisions |
| 85 | Focus Target / Smart Variable |
| 86 | Focus Target / Transform / Position / X (Global) |
| 87 | Focus Target / Transform / Position / Y (Global) |
| 88 | Focus Target / Transform / Position / Z (Global) |
| 89 | Focus Target / Transform / Position / X (Local) |
| 90 | Focus Target / Transform / Position / Y (Local) |
| 91 | Focus Target / Transform / Position / Z (Local) |
| 92 | Focus Target / Transform / Rotation / X (Global) |
| 93 | Focus Target / Transform / Rotation / Y (Global) |
| 94 | Focus Target / Transform / Rotation / Z (Global) |
| 95 | Focus Target / Transform / Rotation / X (Local) |
| 96 | Focus Target / Transform / Rotation / Y (Local) |
| 97 | Focus Target / Transform / Rotation / Z (Local) |
| 98 | Focus Target / Transform / Scale / X (Global) (read-only) /  |
| 99 | Focus Target / Transform / Scale / Y (Global) (read-only) /  |
| 100 | Focus Target / Transform / Scale / Z (Global) (read-only) /  |
| 101 | Focus Target / Transform / Scale / X (Local) |
| 102 | Focus Target / Transform / Scale / Y (Local) |
| 103 | Focus Target / Transform / Scale / Z (Local) |
| 104 | Focus Target / Transform / Child Count (read-only) /  |
| 105 | Focus Target / Rigidbody / Angular Velocity Magnitude (read-only) /  |
| 106 | Focus Target / Rigidbody / Max Angular Velocity |
| 107 | Focus Target / Rigidbody / Mass |
| 108 | Focus Target / Rigidbody / Drag |
| 109 | Focus Target / Rigidbody / Angular Drag |
| 110 | Focus Target / Rigidbody / Max Depenetration Velocity |
| 111 | Focus Target / Rigidbody / Velocity Magnitude |
| 112 | Focus Target / NavMeshAgent / Acceleration |
| 113 | Focus Target / NavMeshAgent / Angular Speed |
| 114 | Focus Target / NavMeshAgent / Base Offset |
| 115 | Focus Target / NavMeshAgent / Velocity Magnitude (read-only) /  |
| 116 | Focus Target / NavMeshAgent / Speed |
| 117 | Focus Target / NavMeshAgent / Height |
| 118 | Focus Target / NavMeshAgent / Radius |
| 119 | Focus Target / NavMeshAgent / Stopping Distance |
| 120 | Focus Target / AudioSource / Doppler Level |
| 121 | Focus Target / AudioSource / Min Distance |
| 122 | Focus Target / AudioSource / Max Distance |
| 123 | Focus Target / AudioSource / Volume |
| 124 | Focus Target / AudioSource / Pan Stereo |
| 125 | Focus Target / AudioSource / Pitch |
| 126 | Focus Target / AudioSource / Reverb Zone Mix |
| 127 | Focus Target / AudioSource / Spread |
| 128 | Focus Target / AudioSource / Spatial Blend |
| 129 | Focus Target / AudioSource / Time |
| 130 | Focus Target / Animator / Float Parameter |
| 131 | Focus Target / Animator / Integer Parameter |
| 132 | Focus Target / Animator / Speed |
| 133 | Focus Target / Animator / Pivot Weight (read-only) /  |
| 134 | Focus Target / Animator / Playback Time |
| 135 | Focus Target / Animator / Left Feet Bottom Height (read-only) /  |
| 136 | Focus Target / Animator / Right Feet Bottom Height (read-only) /  |
| 137 | Focus Target / Animator / Angular Velocity Magnitude (read-only) /  |
| 138 | Focus Target / Physics / Max Ray Distance |
| 139 | Focus Target / Physics / Ray Spacing |
| 140 | Focus Target / Physics / Ray Count |
| 141 | Focus Target / Physics / Ray Vertical Scatter |
| 142 | Focus Target / Physics / Ray Horizontal Scatter |
| 143 | Focus Target / Physics / Max Collisions |
| 144 | NavMeshAgent / Remaining Distance |
| 145 | Focus Target / NavMeshAgent / Remaining Distance |
| 146 | Physics / Last Raycast Hit Normal / X (read-only) /  |
| 147 | Physics / Last Raycast Hit Normal / Y (read-only) /  |
| 148 | Physics / Last Raycast Hit Normal / Z (read-only) /  |
| 149 | Focus Target / Physics / Last Raycast Hit Normal / X (read-only) /  |
| 150 | Focus Target / Physics / Last Raycast Hit Normal / Y (read-only) /  |
| 151 | Focus Target / Physics / Last Raycast Hit Normal / Z (read-only) /  |
| 152 | Transform / Position / Magnitude (read-only) /  |
| 153 | Focus Target / Transform / Position / Magnitude (read-only) /  |
| 154 | Transform / Scale / Magnitude (Local) (read-only) /  |
| 155 | Focus Target / Transform / Scale / (Local) Magnitude (read-only) /  |
| 156 | Transform / Rotation / Magnitude (read-only) /  |
| 157 | Focus Target / Transform / Rotation / Magnitude (read-only) /  |


### Boolean Parameters:

| Index | Value |
| ----- | ----- |
| 0 | True (read-only) /  |
| 1 | False (read-only) /  |
| 2 | Smart Variable |
| 3 | GameObject / Is Active |
| 4 | GameObject / Is Static |
| 5 | GameObject / Has Tag (read-only) /  |
| 6 | Transform / Is Child (read-only) /  |
| 7 | Rigidbody / Is Null (read-only) /  |
| 8 | Rigidbody / Is Sleeping (read-only) /  |
| 9 | Rigidbody / Is Kinematic |
| 10 | NavMeshAgent / Is Null (read-only) /  |
| 11 | NavMeshAgent / Is Enabled |
| 12 | NavMeshAgent / Is On NavMesh (read-only) /  |
| 13 | NavMeshAgent / Is On NavMeshLink (read-only) /  |
| 14 | NavMeshAgent / Is Path Stale (read-only) /  |
| 15 | NavMeshAgent / Is Stopped |
| 16 | NavMeshAgent / Path Pending (read-only) /  |
| 17 | Tween / Is Rotating (read-only) /  |
| 18 | Tween / Is Translating (read-only) /  |
| 19 | Tween / Is Scaling (read-only) /  |
| 20 | Tween / Use Path |
| 21 | Tween / Spinning |
| 22 | Tween / Snappy Scale |
| 23 | Tween / Path In Local Space |
| 24 | Tween / Look At Path |
| 25 | Audio Source / Is Null (read-only) /  |
| 26 | Audio Source / Enabled |
| 27 | Audio Source / Playing (read-only) /  |
| 28 | Audio Source / Virtual (read-only) /  |
| 29 | Audio Source / Looping |
| 30 | Audio Source / Muted |
| 31 | Audio Source / Spatialized |
| 32 | Audio Source / Post Effects Spatialized |
| 33 | Animator / Is Null (read-only) /  |
| 34 | Animator / Enabled |
| 35 | Animator / Applying Root Motion |
| 36 | Animator / Fire Events |
| 37 | Animator / Bool Parameter |
| 38 | Animator / Is Human (read-only) /  |
| 39 | Animator / Is Initialized (read-only) /  |
| 40 | Animator / Is Matching Target (read-only) /  |
| 41 | Animator / Is Optimizable (read-only) /  |
| 42 | Animator / Stabilize Feet |
| 43 | Animator / Is In Transition (read-only) /  |
| 44 | Targets / Has Targets (read-only) /  |
| 45 | Targets / Contains Target With Tag (read-only) /  |
| 46 | Physics / Has Contacts (read-only) /  |
| 47 | Physics / Has Raycast Hits (read-only) /  |
| 48 | Focus Target / Smart Variable |
| 49 | Focus Target / GameObject / Is Null  (read-only) /  |
| 50 | Focus Target / GameObject / Is Active |
| 51 | Focus Target / GameObject / Is Static |
| 52 | Focus Target / GameObject / Has Tag (read-only) /  |
| 53 | Focus Target / Transform / Is Child (read-only) /  |
| 54 | Focus Target / Rigidbody / Is Null (read-only) /  |
| 55 | Focus Target / Rigidbody / Is Sleeping (read-only) /  |
| 56 | Focus Target / Rigidbody / Is Kinematic |
| 57 | Focus Target / NavMeshAgent / Is Null (read-only) /  |
| 58 | Focus Target / NavMeshAgent / Is Enabled |
| 59 | Focus Target / NavMeshAgent / Is On NavMesh (read-only) /  |
| 60 | Focus Target / NavMeshAgent / Is On NavMeshLink (read-only) /  |
| 61 | Focus Target / NavMeshAgent / Is Path Stale (read-only) /  |
| 62 | Focus Target / NavMeshAgent / Is Stopped |
| 63 | Focus Target / NavMeshAgent / Path Pending (read-only) /  |
| 64 | Focus Target / Tween / Is Rotating (read-only) /  |
| 65 | Focus Target / Tween / Is Translating (read-only) /  |
| 66 | Focus Target / Tween / Is Scaling (read-only) /  |
| 67 | Focus Target / Tween / Use Path |
| 68 | Focus Target / Tween / Spinning |
| 69 | Focus Target / Tween / Snappy Scale |
| 70 | Focus Target / Tween / Path In Local Space |
| 71 | Focus Target / Tween / Look At Path |
| 72 | Focus Target / Audio Source / Is Null (read-only) /  |
| 73 | Focus Target / Audio Source / Enabled |
| 74 | Focus Target / Audio Source / Playing (read-only) /  |
| 75 | Focus Target / Audio Source / Virtual (read-only) /  |
| 76 | Focus Target / Audio Source / Looping |
| 77 | Focus Target / Audio Source / Muted |
| 78 | Focus Target / Audio Source / Spatialized |
| 79 | Focus Target / Audio Source / Post Effects Spatialized |
| 80 | Focus Target / Animator / Is Null (read-only) /  |
| 81 | Focus Target / Animator / Enabled |
| 82 | Focus Target / Animator / Applying Root Motion |
| 83 | Focus Target / Animator / Fire Events |
| 84 | Focus Target / Animator / Bool Parameter |
| 85 | Focus Target / Animator / Is Human (read-only) /  |
| 86 | Focus Target / Animator / Is Initialized (read-only) /  |
| 87 | Focus Target / Animator / Is Matching Target (read-only) /  |
| 88 | Focus Target / Animator / Is Optimizable (read-only) /  |
| 89 | Focus Target / Animator / Stabilize Feet |
| 90 | Focus Target / Animator / Is In Transition (read-only) /  |
| 91 | Focus Target / Targets / Has Targets (read-only) /  |
| 92 | Focus Target / Targets / Has Focus Target (read-only) /  |
| 93 | Focus Target / Targets / Contains Target With Tag (read-only) /  |
| 94 | Focus Target / Physics / Has Contacts (read-only) /  |
| 95 | Focus Target / Physics / Has Raycast Hits (read-only) /  |
| 96 | Tween / Billboard Direct Look At |
| 97 | Tween / Billboard Look Horizontal |
| 98 | Focus Target / Tween / Billboard Direct Look At |
| 99 | Focus Target / Tween / Billboard Look Horizontal |
| 100 | Tween / Has Look At Target (read-only) /  |
| 101 | Focus Target / Tween / Has Look At Target (read-only) /  |
| 102 | NavMeshAgent / Auto Braking |
| 103 | Focus Target / NavMeshAgent / Auto Braking |
| 104 | NavMeshAgent / Destination Reached (read-only) /  |
| 105 | Focus Target / NavMeshAgent / Destination Reached (read-only) /  |
| 106 | Smart GameObject / Has Float Variable (read-only) /  |
| 107 | Focus Target / Smart GameObject / Has Float Variable (read-only) /  |
| 108 | Smart GameObject / Has Boolean Variable (read-only) /  |
| 109 | Focus Target / Smart GameObject / Has Boolean Variable (read-only) /  |

