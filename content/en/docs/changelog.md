---
title: Changelog
weight: 1000
---

<!--
## Release 1.2.0
- **Additions**
	- Tools can now be switched to via hotkey (Ctrl+Number)
	- Audio Tool
		- Added mpris media controls on Linux
		- Added function to search for elements
		- Added subscenarios for more structured audio projects
		- Added support for single Spotify tracks in audio elements
		- Added support for audio from YouTube videos in audio elements
		- Added automatic thumbnail generation for audio elements
	- Map Tool
		- Added map markers
	- Combat Tracker
		- Added option to delay a turn

- **Improvements**
	- Improved list header color in dark UI style
	- Audio Tool
		- Removed Spotify elements, instead Spotify playlists/albums/songs can now be added to normal music lists
		- Elements can now have images from the web as thumbnails
		- Thumbnails can be chosen from an unsplash.com collection via dialog
		- UI improvements
		- Projects, categories and scenarios can now be deleted
		- Spotify does not require an official client anymore, [librespot](https://github.com/librespot-org/librespot) is used instead
	- Map Tool
		- Zooming no longer centers the image
		- Zoom steps are now smaller, added slider
		- Maps can now be selected even if the preview image is still loading
  - External Services
    - The Spotify access key is now retrieved from a server. This means you don't have to generate a client id and secret in the Spotify developer console. Though that is still an alternative. Also you can host [the server](https://github.com/philinthegaps/gm-companion-backend) yourself if you want.
    - GoogleDrive integration now works for **all** tools

- **Fixes**
	- Fixed broken info links
	- Fixed element image breaking when file cannot be found, uses default image now
	- Fixed a crash in audio editor when checking for missing files
	- Fixed audio elements not having a mode set by default
	- Fixed bug where the first file in an audio element could not be deleted
	- Fixed Sotify elements needing to be selected a second time to play
	- Fixed GoogleDrive integration not working
-->

## Release 1.1.0
- **Additions**
	- Added random effect table tool to combat tracker. Is currently only available for the DSA5 addon.
	- Addons can now include Spotify playlists and albums
	- Added "Audio Addon" with some great rpg Spotify playlists
	- Audio, maps, shops and characters can now be streamed from Google Drive
		- Audio editor still saves projects locally even with cloud mode enabled
	- Added new optional menu icons (enabled by default)

- **Improvements**
	- Improved audio tool and editor
		- Improved UI
		- Changed default icons
		- Audio editor now has file browser for icons
		- Audio export screen now has a progress bar and no longer freezes the program
		- Audio projects, categories, scenarios and elements can now be renamed
	- Improved map tool
		- Maps can now be rotated
		- Improved UI
	- Improved dice tool UI
		- Result text color is now orange for mixed results instead of dark red / brown
	- Improved combat tracker
		- Removed status field, notes field is now larger
		- INI and health values can now be typed in manually
		- Combat effects now show the dice result
	- Improved shop tool
		- UI is now cleaner and more in line with the rest of the tools
		- Shops can now be renamed
		- Items in shop editor can be filtered by category
	- Improved character tool
		- Added buttons to quickly switch to the next or previous page
		- Added support for PDFs on Linux (Currently not via Google Drive)
	- Improved settings
		- Cleaned up UI
		- Added credits to info page
		- UI style can be changed without restarting
	- Text on Windows version is no longer blurry, though currently there is no fix for the flickering when resizing the Window

- **Fixes**
	- Fixed Spotify integration stops working after an hour or so
	- Fixed Spotify not using custom icons and fetching spotify thumbnail instead
	- Fixed text clipping out of button in Audio Editor on
	- Fixed crashes due to "index out of range" errors in combat tracker

## Release 1.0.2
- **Additions**
	- Added audio cover art showcase

- **Improvements**
	- Audio Editor: When a new path for a missing file was set and the file was found, automatically try this new path with all other missing files
	- Audio Player: Sound playlists are now automatically removed when they have finished
	- Audio Player: Audio element button size is now dynamic and a full row fills all the available space
	- Audio Player: Improved performance
	- Spotify: Auth process is now done in WebEngineView instead of the default web browser

- **Fixes**
	- Fixed Spotify playlists not clearing when changing projects in audio editor
	- Fixed audio volume scale
	- Fixed radios crashing on Linux

## Release 1.0.1
- **Additions**
	- Added alternative menu style

- **Improvements**
	- Moved volume sliders into popup box and made them larger

- **Fixes**
	- Fixed invisible icons

## Release 1.0

- **Additions**
  - **Audio Tool**
    - All files that are actually being used in project can be exported to a folder
    - Added experimental spotify implementation
  - **Tools**
    - Added item shop tool
  - **UI**
    - Added Font Awesome icons

- **Improvements**
  - **Completely reworked UI**
  - **Audio Tool**
    - Editor now marks missing files, if the file was moved the new new folder can be set
    - Linux version now uses TagLib for meta data reading
  - **Map Tool**
    - Now has tabs, maps are now organized in subfolders
  - **Dice Tool**
    - Complete tool overhaul
    - Added visual feedback
  - **Combat Tracker**
    - Complete tool overhaul
  - **Character Tool**
    - Now only displays images of the character sheet
  - **Unit Converter**
    - Complete tool overhaul
    - Custom units can now be removed
  - **Addons**
    - Some addons are now included in the program

## Beta 3.3

- **Additions**
  - Added Combat Tracker and combined it with the dice tool
  - Added sidebar navigation, removed tab system
  - Added changelog to about dialog


- **Removals**
  - Removed Start page


- **Misc**
  - Cleaned up UI
  - Bug fixes

## Beta 3.2

- **Additions**
  - Added [AudioTool](https://github.com/PhilInTheGaps/GM-Companion/wiki/Audio-Tool) that combines the music, sound and radio tools of previous versions
  - Added option to set the font and point size of notes
  - Added loading splashscreen
  - Added logs for easier bug fixing
  - Added new character sheet system that replaces the old one
  - Added "Bonus Dice" feature to the dice tool
  - Added character sheet template feature for addons
  - Added option to show different blog entries (All entries or only entries regarding releases)


- **Improvements**
  - Ubuntu 15.05 and all newer versions are now supported
  - The program is now also available for Ubuntu i386, arm64, armhf and ppc64el systems
  - The notes directory can now be changed
  - Map Viewer now supports mouse dragging
  - Improved settings.ini grouping
  - Improved checking for updates
  - Cleaned up UI of many tools

## Beta 3.1.1

- **Additions**
  - Added notes rot13 encryption
  - Added release notes

- **Improvements**
  - Obsolete files should now be removed when updating to a newer version

- **Fixes**
  - Fixed typos in german translation

## Beta 3.1

- Added unit converter
- Added translation support (Currently only English and German)
- Added grouping feature for music
- Added a second music and sound button style
- Added option to set the amount of generated names
- Fixed glitchy window size on monitors smaller than full hd
- Custom internet radio stations can now be added
- Added Qt-StyleSheet support
- Improved (?) UI
- Added Settings-Window
- Added Notes

## Beta 3.0

- Added rss feed from the [GM-Companion blog](https://philinthegaps.github.io/GM-Companion/)
- Changed media control buttons to have icons instead of text
- Moved media controls to the bottom of the screen to save space
- Added a changelog
- Added support for webradios
- Added music controls when hovering icon in taskbar
- Added name generator
- Added character overview
- Improved Maps-Viewer with zoom function
- Greatly improved memory usage
- Added function to check for updates
- Added function to open wiki
- Added function to report bugs
