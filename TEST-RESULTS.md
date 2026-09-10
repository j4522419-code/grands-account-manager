Validation for version 3 7

Release build and automated tests cover encrypted storage and tamper detection
Bulk imports preserve password text and skip duplicates
Game links and server IDs are checked before launch
Local dummy players verify separate launches and stopping only the selected player
Rejoin uses a fresh process and the saved game target

Display name tests use simulated Roblox replies
They check verified account identity and separate CSRF tokens
They cover unchanged names and rejected names
They cover expired sessions and rate limits
Cancellation prevents a name change
Display names and older data survive encrypted saves

Browser checks load the public login page without submitting credentials
Packaged app checks verify startup and private browser initialization

No real display names were changed
Real authenticated sign in and captcha completion were not tested
Real Roblox joining and rejoining were not tested
The close all Roblox command was not run against real players

Raw test output is in the release folder

Display name checks also cover delayed saves and successful replies without a saved change
An expired session during confirmation never causes another change request


Version selection checks cover installed version ordering and duplicate paths
A selected older version is used and a missing version never falls back silently
The global version choice survives encrypted saves


Previous version download checks cover history parsing and package paths
They verify package checksums and content folders
Missing packages and cancelled downloads never become installed
Partial folders are removed and completed downloads are kept
Archive paths are constrained to the chosen version folder

A complete previous build was downloaded from Roblox servers
Build 0 737 0 7371584 was assembled with the player and content packages
The player was not launched
The download test output is in release download probe results

Copy tests cover single and multiple usernames passwords cookies and combos
Credentials keep their original punctuation and spaces
Right clicking a selected row keeps the multi selection
Right clicking an unselected row selects that row

PIN transfer tests cover leading zero PINs and invalid PIN formats
The correct PIN recovers full account records
Wrong PINs and modified encrypted fields are rejected
Exports contain no plaintext credentials
Each export uses fresh encryption values
Duplicate imports preserve existing accounts
Failed local saves roll back imported accounts

Tests use fictional credentials and do not read or modify the real clipboard
