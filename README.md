Grands Account Launcher

A simple black and white Roblox launcher for Windows

Open GrandsAccountLauncher.exe
No app password is needed
Accounts are saved encrypted for your Windows user

Add account saves a username and password
Bulk add accepts one username and password per line with a colon between them
Passwords keep spaces and extra colons
Duplicate accounts are skipped

Select accounts then choose Display names to give them the same display name
Roblox decides whether the name can be used
If Roblox says to wait the remaining queue stops
You can retry later
The app checks the current name before sending another change

Join game opens a player for each selected account
Rejoin game uses each account last launched game
Enter a server ID if you want to request a specific server
An empty server field lets Roblox choose
There is no fixed delay between launches
Each launch waits for its player window

Sign in opens a separate window in the middle of your screen
Solve any captcha there
An unresponsive login page reloads after ten seconds
It waits while you solve a challenge or type
You can also sign in manually if the page layout changes

Stop selected closes players tracked for those accounts
Close all Roblox force closes every Roblox player including players opened outside this app
Keep the launcher open while using multiple players
After reopening the launcher close existing Roblox players before starting more

Saved accounts stay in the GrandsAccountLauncher folder under LocalAppData
Storage uses AES GCM encryption with a key protected by Windows DPAPI
The previous encrypted save is kept as a backup
Moving to another Windows user can make the saved file unreadable
There is no additional app password
Programs running as your Windows user can access data that user can decrypt

Account creation and groups are removed
Older saved data is preserved inside the encrypted file

Windows x64 and Microsoft Edge WebView2 Runtime are required
The download includes the NET runtime
Roblox must already be installed

To build install PowerShell 7 and NET SDK 10 then run build.ps1
Use the BrowserChecks switch to include the public login page check
Builds and source archives go into the release folder

Tests use fake sessions and local dummy players
Real sign in and game joining need testing with your accounts
See TEST-RESULTS.md for the checks performed

Roblox display name API
https://create.roblox.com/docs/cloud/reference/domains/users

The original MIT license and dependency notices are included
