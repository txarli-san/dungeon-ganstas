# Dungeon Gangstas - Old school text adventure

**DISCLAIMER: This is a recreational project and a work in progress. It is not intended for production use. Expect bugs, incomplete features, and frequent changes. Proceed with no expectations and at your own risk.**

This project is a flexible text adventure game engine written in Ruby. It allows you to create interactive, text-based adventure games with rooms, items, monsters, and various commands.

## Features

- Dynamic room navigation
- Item management (picking up, dropping, and using items)
- Combat system with monsters
- Character stats (health, attack, defense)
- Customizable game data using YAML files
- Extensible command system
- Inventory management
- Randomized item placement and monster loot
- Simple natural language processing for game commands
- Equipment system (weapons, armor, shields)
- Special items and artifacts
- Console and web-based interfaces

## Getting Started

### Prerequisites

- Ruby (version 2.7 or higher recommended)
- Bundler

### Installation

1. Clone this repository:

```
git clone https://github.com/yourusername/ruby-text-adventure.git
```

1.1. Change directory
```
cd ruby-text-adventure
```

2. Install dependencies:

```
bundle install
```

### Running the Game

To start the game in console mode, run:

```
ruby game.rb
```
Or with --debug if you want the minimal version with no TUI:
```
ruby game.rb --debug
```

To start the websocket server for web ui:
```
ruby socket.rb
```

Follow the on-screen prompts to navigate through the adventure.

### Customizing the Game

You can customize the game by editing the `game_data.yml` file in the `data` directory. This file defines rooms, items, monsters, and available commands.

## Project Structure

- `core/`: Core game logic
  - `combat_system.rb`: Manages combat interactions
  - `command_handler.rb`: Handles user input and commands
  - `console_output.rb`: Handles console output
  - `engine.rb`: The main game engine
  - `game_state.rb`: Manages the current game state
  - `game_view.rb`: Handles game view formatting
  - `world.rb`: Generates the game world
- `data/`: Game data files
  - `game_data.yml`: Main game data
  - `items.yml`: Item data
  - `special_items.yml`: Special item data
- `managers/`: Management classes
  - `item_manager.rb`: Manages item-related actions
  - `room_manager.rb`: Manages room navigation and descriptions
- `models/`: Game object models
  - `equipment.rb`: Handles player equipment
  - `inventory.rb`: Manages player inventory
  - `item.rb`: Defines the Item class
  - `player.rb`: Defines the Player class
- `spec/`: Test files
  - `fixtures/`: Test data files
  - Various `*_spec.rb` files for each component
  - `spec_helper.rb`: RSpec configuration
- `utils/`: Utility classes
  - `output_formatter.rb`: Formats output for display
- `game.rb`: Main game loop for console interface
- `socket.rb`: Websocket server for multiplayer functionality
- `server.rb`: TCP server for telnet-like functionality
- `index.html`: Web interface for the game
- `Gemfile` and `Gemfile.lock`: Ruby dependencies

## Running Tests

To run the test suite:

```
rspec
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

lol

## Kudos to:

https://patorjk.com/
