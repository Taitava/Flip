
FFFFF  L      I  PPPP
F      L      I  P   P
FFFFF  L      I  PPPP
F      L      I  P
F      LLLLL  I  P

An implement of a reversi game made by Jarkko Linnanvirta in 2010.

(released on 2010-01-23)

Description
-----------

In Flip your goal is to fill a map so that at the end of the game there are more pawns of your color than pawns of your opponent's color. A pawn can be placed to the map only into a place where it forms a line with one or more pawns of the other color and with another pawn of the same color at the end of the line. All pawns of the different color between the just placed pawn and the pawn with the same color at the end of the line will be flipped to be the same color with the just placed pawn. A line formed by pawns can be horizontal, vertical or diagonal. Placing a pawn can form multiple lines which will all be flipped. A pawn cannot be placed to a place where it won't surround the opponent's pawn(s) with another pawn of the same color.

You can compete against computer or another human. Each player can place only one pawn on his/her turn. If the player has no legal place to put a pawn, an opponent will have a turn *. In this case the game will write a record about the situation into a game log. If the game log is not displayed in the game application, you can see it by selecting Show Game Log from the Settings menu.

If in the above case even the opponent player does not have any legal possibilities to place a pawn, the game will end and winner will be the player with more pawns of his/her color on the map. If there are equal amount of pawns of different colors, the game will be a draw.

*) This is a standard behaviour that are observed by many other reversi games. In Flip you can change this policy through the Settings menu inside the game. Please see the next section for more information.

Features
--------
Some of the game's features are described in the Description section above, so please read that section first.

The game can be played in three modes:
	- Human vs. Human (default setting)
	- Human vs. Computer
	- Computer vs. Computer

You can select player types from the game menus White Player and Black Player. A player type named Randomizer is a simple computer player that decides to place pawns randomly without any special intelligence. In the future versions the game will have more computer player types with better artificial intelligence. A sad story is that I wrote an intelligent computer player but it was not really intelligent and the randomly behaving computer player usually won it. So I decided to exclude that one from the game.

A computer player makes his (or her, if she is a lady computer) decisions fast and moves immediately after human player. Especially if you wach the game in the Computer vs. Computer mode, the whole game will be completed in about two seconds! To make the computer act more like a human, you can enable the CPU waits 2 seconds option from the Settings menu. This tells the computer player type to wait 2000 milliseconds before starting to make any decisions.

If a player cannot place any pawns legally in his/her turn, the game can be configured to do one of the following actions through the Settings menu:
	- Change turn (the default behaviour)
	- Stalemate (the game ends to a state where a player has no legal moves but does not actully loose anything. No one will get score.)
	- Opponent will win (the player who could have a possibility to place a pawns will win the game.)
	- Prosperous player will win (the player who has more pawns of own color currently on the map will win the game.)

Winner of a game will get score one point. If a game ends to a draw or a stalemate, no one gets score but instead a Draw or Stalemate counter gets increased. Both scores and counters of draws and stalemates are showed in the Scores window that can be toggled visible or hidden through the Settings menu.

Current pawn status can be viewed in the Pawns window. This window shows how many pawns the white player has and how many the black player has currently. Also total amount of pawns and amount of empty places on the map are showed in the window. Visibility of the window can be toggled through the Settings menu.

There is also a possibility to save a game to be continued later. Just use the File menu's Save Game and Load Game functions to do this. Each save uses one small file and you can have as many saves as you want. You can even decide a name for the save file! That feature lacks from many commercial PC games that are ported from game consoles. :-)


Graphics
--------

If you don't like the current pawn images (Black.png and White.png), you can change the files to whatever you like - but please keep in mind that their size is fixed to 64x64 pixels. If you change the images, write a note about the change to this ReadMe.txt file! You can also rename the current image files so that the game cannot find them. In this case the game draws solid black and white circles instead of pawn images.

When a pawn is flipped from one color to another, it will play a transition showing the change more fluently. If necessary, the transition can be turned off or on by selecting Animated Pawns from the Settings menu.


Musics
------

All the game musics are located in Music directory. You can add your own music to that directory. Replacing the original musics is also possible. Supported music formats are: raw, mod, s3m, xm, it, mid, rmi, wav, mp2, mp3, ogg, wma, asf and mo3. CAUTION! Some of the stated audio formats does not work properly with CoolBasic's audio engine fmod. Some songs in formats of it and xm (and maybe some others too) MAY cause the game to crash. Unfortunately I cannot do anything for it. Just try different songs and take off the ones that make the game to crash. :-)

The following original music files provided with the game are made and copyrighted by Nody (noby92@luukku.com):
noby_amazonite.xm
noby_gameover.xm
noby_mines.xm
noby_reborn_hero.s3m
noby_stonesmith.s3m

Copying these files without permission from Nody into any other use than in this game application is forbidden. Using them as a part of this game is permitted. Please see Music/DISCLAIMER.txt for further information. Note that DISCLAIMER.txt talks about Modules directory which in case of this game means the Music directory.


Sounds
------

Move.wav is made and copyrighted by Tp (akku@jippii.fi). Using the sound anywhere is only permitted when the stated credits are mentioned with the sound.

Sounds can be replaced with other wav-sounds if you want.


Open Sorce
----------

This game is open source, which means that you can modify and distribute it almost freely. Please see the License chapter for more information about the terms of use, modify and distribute.

The game is programmed with Coolbasic Beta 10.43 which can be downloaded from http://www.coolbasic.com for free. Note that if there are a newer version of CoolBasic available, such as CoolBasic Classic or CoolBasic V3, the newer version is probably not compatible with the game! When CoolBasic Classic becomes available, the game can probably be ported to that language, but it's absolutely more easier to get the game compiled with CoolBasic Beta 10.43 due to differences in syntax rules.

The game uses CoolBasic Software Development Kit function library which provides some interface elements to the application. The functions that Flip uses from CBSDK are copied into cbsdk.cb file so you DO NOT NEED to install CBSDK. Actully CBSDK is not even downloadable from anywhere at the moment.

To be able to compile the game you must download and install CoolBasic. Move or copy all files from Source folder to the game's root directory. This is needed because the game uses media files (sounds, graphics and musics) from the game's root directory. Open Flip.cb into CBEditor and press F5 to compile and run the game. The compilation process takes some time, but after a while the game application should appear on your screen. If the game compiled correctly and you can play the game, then you can start reading the source code and making any modifications you want.

License
-------

This game is Open Source and can be used, modified and shared when obeying all of the following rules:

1. The game application is copyrighted to its original author in those parts that the original author have made himself. Any other parts in the application are copyrighted by their authors and can be used, modified and/or distributed only the way described in their licenses, in this license or in a separate persimission from the author.

2. Any rules mentioned in the Musics chapter, in Music\DISCLAIMER.txt file and in the Sounds chapter must be obeyed.

3. The game or any part(s) of the game cannot be used in any commercial purposes.

4. The parts of the game that are made by the original author of the game (currently including anything but the musics and Move.wav sound file) can be modified freely.

5. The game can be distributed onward. You are not allowed to include with the game any restricted content that is not allowed to be distributed onward. All source code files must be included with the game! If the game is modified, then the modified source code files must be present with the distributed game.

6. You cannot say that you (or somebody else) are the original author of the game if that's not true. Also you cannot claim yourself as an author of any part of the game that you have not made yourself.

7. Anyone who modifies this game can add his own rules to this ruleset BUT he/she cannot change, ban or retain the rules so that other authors of the game (or part(s) of the game) would loose any of their rights to their own made content or work.

8. These rules can be modified any time by the original author of the game or by an author of some part(s) of the game in a way that does not restrict earlier gained rights to content owned by somebody else than the user who modifies the rules.

9. Exceptions to these rules can be asked from and permitted by the game's original author. When making decisions about exceptions, the original author must pay attention to the copyrights of the content in the game that is not made by himself. If an exception is related to a part of the game instead of the whole game, the exception can be asked from and permitted by the author of that part. In this case the author must also pay attention to any copyrights involved in the part he/she is giving permission(s) for.

10. If you use, modify or distribute this game, you indicate that you have read, understood and accepted these rules.


Original author
---------------

I am the original author of the game and my name is Jarkko Linnanvirta. I also use a nickname Jare. You can contact me by email jare@kpelit.net . If you speak Finnish you can also check out the game's website at address http://www.kpelit.net/flip . Currently the site is only in Finnish, but maybe in the future the site will be available in English too.

This game is originally part of the K-pelit production, see more: http://www.kpelit.net (currently in Finnish only). If you want to get more information of the game, me or K-pelit, please send me email in English to the address mentioned above.

Thank you for playing the game!

Regards

Jarkko Linnanvirta