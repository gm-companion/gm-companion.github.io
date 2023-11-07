---
title: Audio
description: Play music and sounds from various sources.
---

![Screenshot of the audio tool](/images/audio-tool-01.webp)

## Audio Projects

Audio project files are located in your audio path, by default _.../your-home-directory/**.gm-companion/audio**_.

They can contain music playlists

### Creating / Editing Audio Projects

Projects can be created and edited using the Editor.
For more information about it see the [Audio Editor](#audio-editor) section.

## Audio Controls

To play an element select a category first. This will display a list of all the available scenarios. Select the scenario you want.

If a music element (music list or radio) is already playing and you want to pause it, click pause.  
To stop a sound list from playing simply click the button that represents the sound in the sidebar.

Note that while you can only play one music list or radio at a time, you can play as many sound lists as you want.  
Starting a music list stops the currently playing radio and vice versa.

## Audio Editor

The Audio Editor can be used to create and edit audio projects.

![Screenshot of the audio editor](/images/audio-editor-01.webp)

### Project Structure

Projects consist of categories, scenarios and [elements](#elements).  
If, for example, your project is named "**Demo Project**" a possible project structure could be the following:

- **Demo Project** (Project Name)
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


#### Elements

The following types of elements are available:

* [Music Lists](#music-lists)
* [Webradios](#webradios)
* [Sound Lists](#sound-lists)

All elements can be customized with icons. For further explanations see the [resources](#resources) section.

##### Music Lists

Music lists consist of one ore more audio files from one of the following sources:

* Local mp3, ogg, etc file
* URL pointing to a file on the internet
* Spotify (track, album, playlist)

They can have one of the following playback modes:

* **Shuffle List**  
All songs are shuffled randomly when the playlist is started. All songs are played once before starting from the beginning.
* **Random Mode**  
Songs are played in a truly random order. It is possible that a few songs are played more often than others.
* **Loop List**  
List is played in sequential order and starts again from the beginning when end is reached.
* **Sequential Order**  
List is played in sequential order. Stops when end is reached.

###### Spotify

{{% alert color="primary" %}}
The Spotify integration requires you to have a Spotify Premium account.
{{% /alert %}}

You can add tracks, albums and playlists to a music list using one of the following formats:

* Spotify URI: `spotify:album:0SHWgw0LPDs37Go6oPdaqp`
* Spotify Link: `https://open.spotify.com/album/0SHWgw0LPDs37Go6oPdaqp`

**Setup**

You can either connect using the default backend server, a custom server or using a local client.
For more information about the backend see [this page](/docs/backend).

Default Server:

1. Go to `Settings -> Accounts -> Spotify`
2. Enter your username and password
3. Click `Connect`

Custom Server:

1. Go to `Settings -> Accounts -> Spotify`
2. Choose "custom server" and enter URL
3. Enter your username and password
4. Click `Connect`

Local Client:

1. Register a Spotify app as a developer:  
    1. Go to [the Spotify developer dashboard](https://developer.spotify.com/dashboard/) and click _"Create a Client ID"_.
    2. Do all the steps and register a new spotify application. The app name and description are not important.
2. Set Redirect URLs:  
    1. Click on your newly registered application and click _"Edit Settings"_.  
    2. Add `http://127.0.0.1:59991/` as a redirect url and save the settings.
3. Get the Client ID and Secret  
    1. Click _"Show Client Secret"_.  
    2. Open the GM-Companion and in the settings page enter your **Client ID** and **Client Secret**.
4. Open GM-Companion and go to `Settings -> Accounts -> Spotify`
5. Enter your username and password
6. Enter your client id and client secret
7. Click `Connect`

##### Sound Lists

Sound lists consist of one ore more audio files from one of the following sources:

* Local mp3, ogg, etc file
* URL pointing to a file on the internet

Multiple sound lists can be played at the same time.

Playback modes are the same as for music lists.

##### Webradios

There are two types of radios supported:

1. **Stream**  
Radios can be streamed directly from a URL.  
Example: _https://play.radiorivendell.com/radio/8000/radio.mp3_
2. **Playlist Files**  
They are stored in the _Radios_ directory (by default _/your/home/**.gm-companion/radios**_). Both **_.m3u_** and **_.pls_** playlists are supported.

## Resources

The resources folder contains custom thumbnails for audio elements.

By default the folder is located here:  
_.../your-home-directory/**.gm-companion/resources**_
