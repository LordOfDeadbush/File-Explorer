# terminal commands: part 1

## Prerequisites

none

## ls

This command shows the list of files in the current directory of the user (in other words, the files in the folder that the user is in)

Let's see an example:

``` shell
D:\SteamLibrary>ls

libraryfolder.vdf  steam.dll  steamapps
```

As we can see in the example above, there are 2 files in the directory and one folder (steamapps) in the directory.

We can also check the files of a specific directory:

``` shell
D:\SteamLibrary>ls steamapps

appmanifest_1091500.acf  appmanifest_1938090.acf  appmanifest_400.acf     appmanifest_677620.acf
appmanifest_1169040.acf  appmanifest_2012840.acf  appmanifest_404790.acf  appmanifest_730.acf
appmanifest_1210320.acf  appmanifest_211820.acf   appmanifest_413150.acf  appmanifest_755500.acf
appmanifest_1275350.acf  appmanifest_2225070.acf  appmanifest_433340.acf  appmanifest_774351.acf
appmanifest_1284210.acf  appmanifest_236390.acf   appmanifest_440.acf     appmanifest_945360.acf
appmanifest_1332010.acf  appmanifest_244930.acf   appmanifest_485450.acf  appmanifest_954850.acf
appmanifest_1349230.acf  appmanifest_255710.acf   appmanifest_552520.acf  common
appmanifest_1468260.acf  appmanifest_289070.acf   appmanifest_578080.acf  downloading
appmanifest_1625450.acf  appmanifest_3590.acf     appmanifest_620.acf     shadercache
appmanifest_1671180.acf  appmanifest_359550.acf   appmanifest_648800.acf  temp
appmanifest_1794680.acf  appmanifest_386180.acf   appmanifest_667970.acf  workshop
```

As we can see, there are a lot of files here! We can run ls on any directory provided that we have the path to the directory.

``` shell
C:\Users\agumm>ls D:\SteamLibrary\steamapps\common

 5dchesswithmultiversetimetravel    Muck                      SNOW
'Among Us'                          Necesse                  "Sid Meier's Civilization VI"
'Call of Duty HQ'                  'Ninja Kiwi Archive'      'Slime Rancher'
 Cities_Skylines                   'ONE PIECE WORLD SEEKER'   Splitgate
 Citystate                          PUBG                      Starbound
'Counter-Strike Global Offensive'  'Plants Vs Zombies'       'Stardew Valley'
 Crossout                           Portal                    Stray
'Cyberpunk 2077'                   'Portal 2'                'Team Fortress 2'
 FarCry5                            PortalRTX                "Tom Clancy's Rainbow Six Siege"
'Godot Engine'                     'Potion Craft'             Trackmania
'Guild Wars 2'                      Raft                     'VTOL VR'
'Kerbal Space Program 2'           'Ricochet Ranger'         'Vampire Survivors'
'Leaf Blower Revolution'           'SC Jogos'                'War Thunder'
```

## cd

This command allows us to navigate to different directories. We can see the current directory in terminal right next to where we are typing:

``` shell
D:\SteamLibrary>
```

The following is an example on how to change directories. We will move from our current directory to the steamapps directory:

``` shell
D:\SteamLibrary>ls

libraryfolder.vdf  steam.dll  steamapps

D:\SteamLibrary>cd steamapps

D:\SteamLibrary\steamapps>ls

appmanifest_1091500.acf  appmanifest_1938090.acf  appmanifest_400.acf     appmanifest_677620.acf
appmanifest_1169040.acf  appmanifest_2012840.acf  appmanifest_404790.acf  appmanifest_730.acf
appmanifest_1210320.acf  appmanifest_211820.acf   appmanifest_413150.acf  appmanifest_755500.acf
appmanifest_1275350.acf  appmanifest_2225070.acf  appmanifest_433340.acf  appmanifest_774351.acf
appmanifest_1284210.acf  appmanifest_236390.acf   appmanifest_440.acf     appmanifest_945360.acf
appmanifest_1332010.acf  appmanifest_244930.acf   appmanifest_485450.acf  appmanifest_954850.acf
appmanifest_1349230.acf  appmanifest_255710.acf   appmanifest_552520.acf  common
appmanifest_1468260.acf  appmanifest_289070.acf   appmanifest_578080.acf  downloading
appmanifest_1625450.acf  appmanifest_3590.acf     appmanifest_620.acf     shadercache
appmanifest_1671180.acf  appmanifest_359550.acf   appmanifest_648800.acf  temp
appmanifest_1794680.acf  appmanifest_386180.acf   appmanifest_667970.acf  workshop
```

We can also navigate to a parent directory using ```cd ..```

``` shell
D:\SteamLibrary\steamapps>ls

appmanifest_1091500.acf  appmanifest_1938090.acf  appmanifest_400.acf     appmanifest_677620.acf
appmanifest_1169040.acf  appmanifest_2012840.acf  appmanifest_404790.acf  appmanifest_730.acf
appmanifest_1210320.acf  appmanifest_211820.acf   appmanifest_413150.acf  appmanifest_755500.acf
appmanifest_1275350.acf  appmanifest_2225070.acf  appmanifest_433340.acf  appmanifest_774351.acf
appmanifest_1284210.acf  appmanifest_236390.acf   appmanifest_440.acf     appmanifest_945360.acf
appmanifest_1332010.acf  appmanifest_244930.acf   appmanifest_485450.acf  appmanifest_954850.acf
appmanifest_1349230.acf  appmanifest_255710.acf   appmanifest_552520.acf  common
appmanifest_1468260.acf  appmanifest_289070.acf   appmanifest_578080.acf  downloading
appmanifest_1625450.acf  appmanifest_3590.acf     appmanifest_620.acf     shadercache
appmanifest_1671180.acf  appmanifest_359550.acf   appmanifest_648800.acf  temp
appmanifest_1794680.acf  appmanifest_386180.acf   appmanifest_667970.acf  workshop

D:\SteamLibrary\steamapps>cd ..

D:\SteamLibrary>ls

libraryfolder.vdf  steam.dll  steamapps
```

We can also use paths similarly to ls:

``` shell
D:\SteamLibrary>cd D:\SteamLibrary\steamapps\common

D:\SteamLibrary\steamapps\common>
```

Note: to change drives in Windows you need to type the drive letter like so:

``` shell
C:\Users\agumm>D:

D:\>
```

## How to do this in Python

In python, one of the built-in libraries, os, has a function called ```system``` which can be used to execute commands:

``` python
import os # will give us all of the functions from the os library

# echo is basically the terminal version of print
os.system("echo hello world")

# what this will show in terminal:
'hello world'

# what this will return:
0
```

The issue here is that os.system does not return the result of the command, but rather the exit code.

The solve for this is to use the ```subprocess``` module, and I have included a link for y'all to figure that out:

![link](https://stackabuse.com/executing-shell-commands-with-python/)

happy hunting!

corn
