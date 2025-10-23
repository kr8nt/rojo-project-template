# rojo-project-template
This template contains pre-configured rokit, selene, stylua and wally, to clone it and immediatelly start working on your new Rojo project.

## Setup
1. Clone the repo
2. Install rokit on Linux
 ```
 curl -sSf https://raw.githubusercontent.com/rojo-rbx/rokit/main/scripts/install.sh | bash
 ```
4. Install pre-configured tools with rokit
```
rokit install
```
6. Initialize Rojo
```
rojo init
```

That's it, now you can start working on your awesome project!

## Publishing to Roblox using Open Cloud API
If you don't have access to studio and still want to test the game, you can publish it to Roblox using Open Cloud API.

To publish a game, you need an already created place on Roblox (through Roblox Studio).
**Be aware, that publishing a game to Roblox will override everything you already had in that place!**

Create a .env file in the root of the repo and add the following variables:
1. PLACE_ID - The ID of the place
2. UNIVERSE_ID - The ID of the experience
3. RBXCLOUD_API_KEY - Your Roblox API key

When publishing a game, load env variables and then run the publish command (command is below in Useful commands)

## Luau Language Server
If using the Luau Language Server extension, to make it work, open a new terminal and use this command:
```
rojo sourcemap --watch default.project.json --output sourcemap.json
```

## List of tools
1. Rokit - Toolchain manager
2. Rojo - Build tool
3. Wally - Package manager
4. rbxcloud - CLI and library for Roblox Open Cloud API 
5. StyLua - Code formatter
6. selene - Linter
7. luau-lsp - Language server

## Useful commands
Build Rojo game file
```
rojo build --output=build/game.rbxlx
```

Load env variables
```
set -a; source .env; set +a
```

Publish game to Roblox
```
rbxcloud experience publish --filename build/game.rbxlx --place-id $PLACE_ID --universe-id $UNIVERSE_ID --version-type published
```

## Useful Extensions
To use all tools in this template, we also need to install these extensions:
```
https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.stylua
https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml
https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.luau-lsp
```
