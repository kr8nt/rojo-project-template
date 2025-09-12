# roblox-game-template
Template for a new Roblox game that uses Rokit as a toolchain manager, Rojo for file sync, Wally for package management and rbxcloud for publishing the game builds to Roblox.

## Setup
This is a short list of steps that need to be done to get a new workspace ready for working on the game.

### 1.) Install Rokit
To install Rokit on Linux use this:
```
curl -sSf https://raw.githubusercontent.com/rojo-rbx/rokit/main/scripts/install.sh | bash
```

### 2.) Install tools
To install all of the pre-added tools (```rokit.toml```), use this:
```
rokit install
```

## Useful commands
- Building Rojo game file:
```
rojo build --output=build/game.rbxlx
```

- Publishing game build:
```
rbxcloud experience publish --filename build/game.rbxlx --place-id $PLACE_ID --universe-id $UNIVERSE_ID --version-type published
```

Don't forget to create .env and add PLACE_ID, UNIVERSE_ID, RBXCLOUD_API_KEY and then loading all of these env variables using:
```
set -a; source .env; set +a
```

## Useful Extensions
To use all tools in this template, we also need to install these extensions:
```
https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.stylua
https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml
https://marketplace.visualstudio.com/items?itemName=JohnnyMorganz.luau-lsp
