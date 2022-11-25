---
title: Name Generator
subtitle:
---

![](/images/name-generator-01.png)

## Usage

As the name suggests, the "Name Generator" lets you generate some names for characters.

To generate them use the spin box to set the amount of names to be generated. (Default value is 15)  
Select a category, click the button for the type name you want to generate.  
Done.

To generate new names click the button again.

## Custom Names

The name generator works by selecting a random one from a list of names and combining it with a last name that is also randomly selected.

To add your own names go into the _.gm-companion_ folder located in your home directory.  
Names are placed in categories, the default one being _Generic_.  
If you want to create a new category simply create a new folder in the _names_ subfolder.  
Inside that folder create another one for the type of names you want to add.  

**Example:**  
For this example we will create a new category and name it "Example".  
Now we have the following directories: _/.gm-companion/names/Example_.  
We now want to add a name generator for dwarf names and to do that we create a new folder "Dwarves".  
We need to create 3 textfiles in the _Example/Dwarves_ folder:  
* _male.txt_
* _female.txt_
* _surnames.txt_

Those files include the actual names, seperated by a ",". (No spaces!)  
For this example we will open _male.txt_ and add the following line:  
`Bifur,Bofur,Bombur`  
If you want to add female names or surnames do so in a similar fashion.

If you add names for a culture that does not use surnames or is female only or something similar, delete the unused files.

## Names in Addons

Addons can add their own category of names if they are enabled in the options.  
Addon names are not located in the _names_ folder but instead in the addon folder.  
For more information about addons visit the [addon page](/docs/addons)
