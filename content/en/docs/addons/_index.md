---
title: Addons
no_list: true
weight: 4
---

Addons can be enabled or disabled in the settings.  
Changing those settings requires a program restart.

## Features

Addons can use the following features (they don't have to):

- Custom Maps
- Items and shops
- Name generators
- Units for the converter

## Available Addons

RPG system addons are fanware and not official!

Addons for the following RPG systems are available:

- [DSA 5](/documentation/addons/dsa5.html) (German only)
- [A Song of Ice and Fire Roleplaying](/documentation/addons/sifrp.html)

Other addons:

- [Audio Addon](/documentation/addons/audio.html)

## Custom Addons

Custom addons can be installed by extracting the archive to the _"Addons"_ directory. (By default _/your/home**/.gm-companion/addons**)_

## Creating Addons

Currently creating addons is a bit of a hassle, but there are plans to create a seperate tool for easier addon creation in the future.

### Getting started

Create a new folder in the "Addons" directory.  
In your folder create a new file _**addon.ini**_.  
Open the file in a text editor and paste the following:

```
[General]
name="My_Addon"
description="My_Addon_Description"
addons_version=3
```

Where *My_Addon* is the name of your addon and *My_Addon_Description* a short description of it.  
Do not edit the *addons_version* number!

Now the GM-Companion should recognize your addon!

### Audio

Addons can include links to Spotify playlists or albums.

1. Create a file named _spotify.json_ inside your folder.
2. Copy the following template to the file:  
```
{
	"data": [
		{
			"folder": "The name of your addon or some other name",
			"playlists": [
                {
                    "name": "Playlist 1",
                    "uri": "spotify:album:###############"
                },
                {
					"name": "Playlist 2",
					"uri": "spotify:album:###############"
				}
            ],
			"albums": [
				{
					"name": "Album 1",
					"uri": "spotify:album:###############"
				},
				{
					"name": "Album 2",
					"uri": "spotify:album:###############"
				}
			]
		}
	]
}
```
Example Spotify URI: _spotify:album:6bNTAa9CqIDv3pycA2eH8f_
3. Modify the file and add your albums and playlists.

### Maps

Adding maps to your addon is simple:

Inside your folder create a new subfolder: _**maps**_  
Now simply copy all the maps you want to include to that folder.

The maps tool will have them in a category with the name of your addon.

### Units

The easiest way to add units to your addon is by doing the following:

1. Go to the following directory: _/your/home**/.gm-companion/units**)_ and rename the file _**custom2.ini**_ to something else.
2. Open the GM-Companion and add all the units you want for your addon as custom units in the converter tool.
3. Copy the new _**custom.ini**_ file to your addon folder and rename it to _**units.ini**_. Now you can go back and change the name of _**custom2.ini**_ back to _**custom.ini**_.

Unfortunately you are not done yet!  
Open the _**units.ini**_ file in a text editor.  
The file will look something like this:

```
[LengthUnits]
1\category=Custom
1\name=Test Unit 1
1\refUnits=12
2\category=Custom
2\name=Test Unit 2
2\refUnits=25
size=2
```

A unit consists of 3 parts: The name, refUnits and the category.  You don't want your units to be in the "Custom" category, so go ahead and change the name of the categories to something like **"(MyAddon) Cool Units"**.  

### Names

1. Create a new folder _**names**_ in your addon folder.
2. Create a new subfolder for each type of name, for example: _Humans_, _Elves_ ...
3. Inside these subfolders create (some) of the following files:
- male.txt
- female.txt
- surname.txt  
If for example you don't need surnames for your type then you don't need to create _surname.txt_.
4. Write all possible names in the respective files like this:  
_male.txt:_ `Bob,Frank,Paul`  
Be sure to seperate the names with a "," and do not leave a witespace behind it!

### Items and Shops

For items and shops we have to do a similar workaround as with units.

#### Items

1. Go to the following directory: _/your/home**/.gm-companion/shop**)_ (If you have set a custom shop path in the settings use your custom one) and rename _**CustomItems.items**_ to _**CustomItems2.items**_ or something else.
2. Use the item editor to add all the items you want. When you are done move the new _**CustomItems.items**_ file to your addon folder and rename the file to _**AddonItems.items**_.
3. Go back and rename _**CustomItems2.items**_ back to _**CustomItems.items**_.

#### Shops

You can simply create the shops in the shop editor and then move the _**.shop**_ files to the shop folder inside your addon folder.
