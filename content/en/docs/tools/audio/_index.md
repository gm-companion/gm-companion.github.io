---
title: Audio
---

This chapter is about using the audio tool to play music, sounds, webradios or spotify playlists from an audio project. For instructions on how to create a project please refer to the [Audio Editor chapter](#audio-editor).

![](/images/audio-tool-01.png "Screenshot of the audio tool")

## Audio Projects

Audio project files are located in your "Audio Projects" path, by default _.../your-home-directory**/.gm-companion/audio**_

### Opening Audio Projects

Use the project combo box on the left to select a project.  
It will open automatically.

### Creating / Editing Audio Projects

Projects can be created and edited in the Editor.
For more information about it see the [Audio Editor](#audio-editor) section.

## Audio Controls

### Playing an Element

To play an element select a category first. This will display a list of all the available scenarios. Select the scenario you want.

If a music element (music list or radio) is already playing and you want to pause it, click pause.  
To stop a sound list from playing simply click the button that represents the sound in the sidebar.

Note that while you can only play one music list, radio or Spotify playlist at a time, you can play as many sound lists as you want.  
Starting a music list stops the currently playing radio and vice versa. Music lists, radios and Spotify playlists cannot be played at the same time.

### Changing the current song

Click the "Next" button to switch to the next song in a music list.  
If you want to switch to a specific song select one in the playlist. (You might have to open the sidebar for that.)

# Audio Editor

The Audio Editor can be used to create and edit projects for the [Audio Tool](#audio-tool).

![](/images/audio-editor-01.png "Screenshot of the audio editor")

## Project Structure

Projects consist of categories, scenarios and [elements](#elements).  
If, for example, your project is named "**Pen&Paper**" a possible project structure could be the following:

- **Pen&Paper** (Project Name)
  - **Fantasy** (Category)
    - **Situations** (Scenario)
      - **Travel** (Music List)
    - **Places** (Scenario)
      - **City** (Music List)
      - **City** (Sound List)
      - **Tavern** (Music List)
      - **Tavern** (Sound List)
      - **Docks** (Sound List)
    - **Weather** (Scenario)
      - **Rain** (Sound List)
      - **Snow** (Sound List)
    - **Generic Music** (Scenario)
      - **Radio Rivendell** (Radio)
  - **Science Fiction** (Category)
    - Some content ...
  - **Something else** (Category)
    - Also some content ...


### Elements

There are the following types of elements available:

Offline:
* [Music Lists](#music-lists)
* [Sound Lists](#sound-lists)

Streaming:  
* [Webradios](#webradios)
* [Spotify Playlists](#spotify)

All elements can be customized with icons. For further explainations see the [**resources**](/docs/tools/audio/resources) page.

#### Music Lists

Only one music list can be played at a time. Music lists cannot be played together with webradios or Spotify playlists.  
They can have one of the following playback modes:
* **Shuffle List**  
All songs are shuffled randomly when the playlist is started. All songs are played once before starting from the beginning.
* **Random Mode**  
Songs are played in a truly random order. It is possible that a few songs are played more often than others.
* **Loop List**  
List is played in sequential order and starts again from the beginning when end is reached.
* **Sequential Order**  
List is played in sequential order. Stops when end is reached.

#### Sound Lists

Multiple sound lists can be played at the same time. They can also be played together with music lists, webradios or Spotify playlists.  
They can have one of the following playback modes:
* **Shuffle List**  
All sounds are shuffled randomly when the playlist is started. All sounds are played once before starting from the beginning.
* **Random Mode**  
Sounds are played in a truly random order. It is possible that a few sounds are played more often than others.
* **Loop List**  
List is played in sequential order and starts again from the beginning when end is reached.
* **Sequential Order**  
List is played in sequential order. Stops when end is reached.

#### Webradios

Webradios cannot be played together with music lists or Spotify playlists.  
There are two types of radios supported:
1. **Stream**  
Radios can be streamed directly from an URL.  
Example: _http://radiorivendell.ddns.net:8000/128kbit.mp3_
2. **Playlist Files**  
Playlist files can be used by switching to _Local Mode_.  
They are stored in the _Radios_ directory (by default _/your/home**/.gm-companion/radios**_). Both **_.m3u_** and **_.pls_** playlists are supported.

#### Spotify

Because of the way the new Spotify API works, the GM-Companion is only able to control a Spotify application running in the background. Direct playback of Spotify content is not supported.  
Because there is no server backend for the GM-Companion Spotify authorization can only be done by having access to a developer Client ID and a Client Secret Key.

How to use Spotify in the GM-Companion:

1. **Register a Spotify app as a developer**  
Go to [the Spotify developer dashboard](https://developer.spotify.com/dashboard/) and click _"Create a Client ID"_  
Do all the steps and register a new spotify application. The app name and description are not important.  

2. **Set Redirect URLs**  
Click on your newly registered application and click _"Edit Settings"_.  
Add _http://127.0.0.1:59991/_ as a redirect url and save the settings.

3. **Get the Client ID and Secret**  
Click _"Show Client Secret"_.  
Open the GM-Companion and in the settings page enter your **Client ID** and **Client Secret**.

4. **Start a Spotify client**  
Due to restrictions in the API the GM-Companion cannot play Spotify playlists directly, only control an official Spotify client.  
Open the Spotify app or desktop program and play a song to set it as your active spotify client.  

5. **Add a Spotify playlist (or album)**  
Currently only playback of playlists or albums is supported.  
Use the editor to add a new Spotify playlist element. The chosen name is not important.  
Enter a valid Spotify URI. This can be either a playlist or album URI and can be obtained in the Spotify client.  
Find a playlist or album you want to use, click _Share_ and then _Copy Spotify URI_. The URI looks something like this:  
**Playlist:** spotify:user:radiorivendell:playlist:422FnvL2Q92mvDfzeIlyiW  
**Album:** spotify:album:0SHWgw0LPDs37Go6oPdaqp

Note: If you don't select a custom local thumbnail, it will be fetched from Spotify.
