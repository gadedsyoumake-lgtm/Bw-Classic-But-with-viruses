# BonziWORLD Classic

## Overview
BonziWORLD Classic is a revival of the BonziWORLD chat application. Users can join public or private chat rooms using animated Bonzi Buddy characters with text-to-speech powered by espeak.js.

## Project Architecture
- **Runtime**: Node.js (Express + Socket.io)
- **Entry Point**: `index.js` - starts Express server and Socket.io
- **Static Files**: `build/www/` - pre-built client-side assets (HTML, CSS, JS, images)
- **Server Modules**:
  - `meat.js` - Core chat logic (rooms, users, commands)
  - `ban.js` - Ban/kick management
  - `console.js` - Server console commands
  - `log.js` - Winston logging
  - `utils.js` - Helper functions
- **Config**: `settings.json` - server settings, room defaults, port config
- **Port**: 5000 (configured in settings.json)

## Key Files
- `index.js` - Express server setup, socket.io init, serves static files from `build/www/`
- `meat.js` - Room and User classes, chat commands (/joke, /color, /name, etc.)
- `settings.json` - All server configuration
- `bans.json` - Active ban list (auto-created)
- `build/www/index.html` - Client entry point

## Recent Changes
- Configured port to 5000 for Replit environment
- Created missing client-side placeholder files (speakClient.js, angular.js, yt_widget_api.js, platform.css, cordova.js)
- Added .gitignore for node_modules and logs
