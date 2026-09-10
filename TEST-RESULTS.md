Validation for version 3 4 1

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

