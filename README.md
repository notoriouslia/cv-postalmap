# CV Postal Map

A custom postal map and navigation resource built for FiveM.

This resource replaces the normal GTA V map setup with a custom postal-based system designed for Carson Valley. It includes custom postal data, street names, navigation commands, voice feedback, and support for streaming a custom map texture.

Features
Custom postal system
Custom street name data
/postal and /p navigation commands
Automatically places a waypoint at the requested postal
Voice confirmation when starting a route
Arrival notification when reaching your destination
Automatically clears the route once you arrive
Custom configurable navigation settings
Support for custom streamed map textures
Included postal and street JSON data
Map generation tools included
Commands
/postal [number]

Creates a route to the specified postal.

Example:

/postal 1024
/p [number]

Shortened version of the postal command.

Example:

/p 1024

Once a valid postal is entered, the resource will create a waypoint to that location and provide voice feedback confirming the route.

When you arrive near the postal, the route will automatically clear.

Installation
Download or clone the resource.
Place the cv-map folder inside your FiveM resources folder.
resources/[maps]/cv-map
Add the resource to your server.cfg.
ensure cv-map
Restart your server.
File Structure
cv-map/
├── client/
│   ├── main.lua
│   ├── map.lua
│   ├── navigation.lua
│   └── voice.lua
│
├── html/
│   ├── audio/
│   ├── index.html
│   └── script.js
│
├── shared/
│   ├── postals.json
│   ├── streets.json
│   └── Streets_lc.json
│
├── stream/
│
├── tools/
│   ├── generate_map.py
│   └── requirements.txt
│
├── config.lua
└── fxmanifest.lua
Configuration

Most settings can be changed through:

config.lua

This allows the resource to be adjusted without having to rewrite the main client files.

Postal locations are stored inside:

shared/postals.json

Street information is stored inside:

shared/streets.json
Custom Map

The resource is designed to support a custom streamed FiveM map/minimap.

Any required map assets should be placed inside the:

stream/

folder.

A map generation utility is also included under:

tools/generate_map.py

for generating or preparing map-related assets.

Requirements
FiveM
A properly configured FiveM server
Custom map assets if you intend to use the map replacement portion

The main resource itself is designed to remain lightweight and simple to install.

Notes

This resource was specifically created for Carson Valley and uses custom postal and street data.

If you are using this resource for another community, you will most likely need to replace the provided postal, street, and map data with your own.

Credits

Developed for Carson Valley.

Please do not redistribute, resell, or reupload the resource without permission.
