Match'em Poker XNA 1.1
======================

Match'em Poker is a traditional match3-type game with a twist: Instead of 
matching blocks of the same colour, the player is matching different poker 
hands. The game is a port from the Qt version which, in turn, is a port from 
the original iOS version. 

When porting, the intent was to do so with minimal effort, reusing everything 
possible. The code is NOT originally written with C# nor for WP7. 


PLAYING MATCH'EM POKER
-------------------------------------------------------------------------------

The game is played in a rectangular grid. The player can swap the position of 
any two cards. When a 'poker hand' is formed, it will disappear from the level 
and the player's score increases. A card will drop down if there is an empty 
space below it. New cards will appear in empty spaces in the first row. The 
level starts with a timer value of 40. This number decreases with time, and 
increases when the player scores. The level is completed when the timer 
reaches a value of 100. If the timer drops to zero, the game is over.
 
Accepted 'hands' are: 
   - 4 or more of the same color
   - 3 or more of the same number
   - a straight of 4 or more

Accepted 'hands' are: 4 or more of the same colour, 3 or more of the same 
number, a straight of 4 or more. The hands can appear either horizontally or 
vertically. The difficulty increases when the player reaches higher levels. 
The time spent will affect the timer more and more, and destroyed cards will 
increase the timer less and less. Theoretically the game can continue forever. 
In practice, it will get very difficult around level 20.

There are increasing numbers of empty cards in the levels. An empty card will 
not be accepted to be a part of a hand until it's opened (by clicking it). 
When an empty card is opened, a small amount of time is removed from the timer 
(as a payment).


PREREQUISITES
-------------------------------------------------------------------------------

- C# intermediate
- Development environment 'Microsoft Visual Studio 2010 Express for Windows 
  Phone'


LINKS
-------------------------------------------------------------------------------

Getting Started Guide:
http://create.msdn.com/en-us/home/getting_started

Learn About Windows Phone 7 Development:
http://msdn.microsoft.com/fi-fi/ff380145

App Hub, develop for Windows Phone:
http://create.msdn.com

Game Development:
http://create.msdn.com/en-us/education/gamedevelopment


IMPORTANT FILES/CLASSES
-------------------------------------------------------------------------------

source files:

- Game1.cs: A main application class for the game
- TileInterfaces: Interfaces for game and engine, some commonly used 
enumerations
- ParticleEngine.cs: Consists of three classes; Particle, ParticleSpray, and 
ParticleEngine. Simulates particles and handles drawing them on the screen.
- npclevel.h: The match-grid-game part of the application
- tilenpc.h: Implementation of interface ITileGame. The platform-independent
main game.
TileGameRendererXNA.cs: XNA implementation of an ITileRenderer interface which 
works as the engine for the framework. Rendering is implemented using XNA's 
SpriteBatch object.


KNOWN ISSUES
-------------------------------------------------------------------------------

None.


BUILD & INSTALLATION INSTRUCTIONS
-------------------------------------------------------------------------------

Preparations
~~~~~~~~~~~~

Make sure you have the following installed:
 * Windows 7, may also work on Windows XP
 * Microsoft Visual Studio 2010 Express for Windows Phone
 * The Windows Phone Developer Tools January 2011 Update:
   http://download.microsoft.com/download/6/D/6/6D66958D-891B-4C0E-BC32-2DFC41917B11/WindowsPhoneDeveloperResources_en-US_Patch1.msp
 * Windows Phone Developer Tools Fix:
   http://download.microsoft.com/download/6/D/6/6D66958D-891B-4C0E-BC32-2DFC41917B11/VS10-KB2486994-x86.exe


Build on Microsoft Visual Studio
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Open the SLN file:
   File > Open Project, select the file XNAPuzzlePoker.sln.
2. Select the 'Windows Phone 7 Emulator' target.
3. Press F5 to build the project and run it on the Windows Phone Emulator.


Deploy to Windows Phone 7
~~~~~~~~~~~~~~~~~~~~~~~~~

Preparations:
1. Register in the App Hub to get a Windows Live ID:
   http://create.msdn.com/en-us/home/membership
2. Install Zune for Windows Phone 7:
   http://www.zune.net/en-us/products/windowsphone7/default.htm
3. Register your device in your Windows Live account. 
   Select from Windows: Start > Windows Phone Developer Tools > Windows Phone 
   Developer Registration

Deploy:
1. Open the SLN file:
   File > Open Project, select XNAPuzzlePoker.sln file.
2. Connect the device to Windows via USB.
3. Select the 'Windows Phone 7 Device' target.
4. Press F5 to build the project and run it on your Windows device.

   
COMPATIBILITY
-------------------------------------------------------------------------------

- Windows Phone 7
- XNA Game Studio 4.0

Tested on: 
- HTC 7 Mozart
- Samsung Omnia 7

Developed with:
- Microsoft Visual Studio 2010 Express for Windows Phone


CHANGE HISTORY
-------------------------------------------------------------------------------

1.1 Code style and convention fixes
1.0 The first non-beta version
0.9 Release candidate 1