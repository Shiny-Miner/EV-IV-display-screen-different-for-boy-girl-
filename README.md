# Custom-EV-IV-Display-Screen (Terry's Vertion)Ver. 1.5 2022.
 Customizable template to display information on the EV, IV and BS of our pokemon team in a new
 screen.

 This is a Modification of the Custom EV - IV Display Screen of Azimut which includes some
 aesthetic changes that the original version does not have.
 
(The files inside the src\include\ folder were taken from pokefirered.)
 
Features (Azimuth Version):
-
+ Compatible with Pokémon Fire Red, Fire Red and Emerald.
+ You can change the background by replacing the default one, the injection will insert it
  automatically.
+ You can change the coordinates of the pokemon sprite, as well as its texts.
+ The color of the IVs stat changes according to nature.
+ Shows base statistics according to the species.
+ Censors the eggs stat, instead it says approx. How many steps do you need to hatch?
+ Very cute and with little sleepies xd
+ Smells like lemon.
+ base: Pokémon Fire Red.


Uncle Terry's version (Mia):
-
+ Continues to be compatible with Fire Red, Fire Red and Emerald.
  (For now).
+ 2 colors for Boy and Girl.
  (Configured according to the gender of the protagonist).
+ Reorganization of texts.
+ Natures with name and indicators with their respective color.
+ Level, Gender and Types of the Pokémon.
+ Type of Hidden Power according to the sum of Ivs.
+ Team PokéBalls.
  (The Pokeball of the selected Pokémon will open).
+ The background, the Name, the Level of the Pokémon will turn yellow if the Pokémon is Shiny.
+ It continues to be cute and with more sleepiness xd
+ Preserves the smell of Lemon.
+ base: Pokémon Fire Red.

***Notes:***
For simple setups here is the most fundamental thing to do to compile and use InGame:

- DevkitARM and ARMIPS are required (newer versions).

- To compile it is necessary to have preproc.exe and gbagfx.exe inside some path of the PATH variable

- Open the config.mk file, find and change ff0000 in the following line to an offset aligned with
  enough free space (more than 0x2000 bytes):
        `INSERT_INTO ?= 0x08ff0000`
- In the config.mk file, also look for the following line
        `ROM_CODE ?= BPRE`
        - leave BPRE to compile using Fire Red
        - switch to BPRS to compile using FireRed
        (If you use Fire Red go here to see the main_eviv.c file configuration)
        - switch to BPEE to compile using Emerald
        (If you use Emerald go here to see the main_eviv.c file configuration)

- Build by running make with your terminal, and a rom with the injection will appear in a folder called
  build (It will have the name according to the Version of the game that you just placed in the config.mk file).

- Use in a script `callasm` followed by the offset+1 where they inserted the code.

- Files inside the include folder were taken from pokefirered.

