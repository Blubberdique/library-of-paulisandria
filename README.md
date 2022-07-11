# Library of Paulisandria
Made by Gerlach

## Welcome to the library of Paulisandria! 
This is my library of Digispark and Rubber Ducky payloads, and a repository I made for those interested in learning how to code either through Arduino for the Digispark, or through Ducky Script for the Rubber Ducky.



## Tutorials

The file "---.txt" contains the basics for writing and deploying a payload to the Digispark USB, and can be found in ".\Tutorials\Digispark\General".

The file "---.txt" contains the basics for writing and deploying a payload to the Rubber Ducky, and can be found in ".Tutorials\Rubber Ducky\General".

The file "Digispark-keystrokes.txt" contains the method to keybinding and a list of possible keybinds for the Digispark USB, and can be found in the root folder.



## (GIVE-HEADER-NAME)
All payloads will be supplied in both .TXT and .INO formats, so that there is a ready-to-deploy and an editable variant of every payload.



## Basics for payload buildup

Always include the line #include "DigiKeyboard.h" , as this allows the Digispark to send keystrokes (it otherwise will have just a .ino file without any references). 

To make comments, there are two ways of going about it. There is the single line comment, which goes as following:
// This is an example comment.

Then there is the multi line comment, which goes as following:
/*
    This is a multi line comment.
    It can be useful from time to time.
*/



## Basic Digispark payload

Basic example:

	#include "DigiKeyboard.h"

	void setup() {
    		// Left empty.
	
	}

	void loop() {

    		DigiKeyboard.print();
    		DigiKeyboard.sendKeyStroke();
    		DigiKeyboard.delay(1000);

    		// Opens up a browser and goes to a David Bombal video.

    		DigiKeyboard.sendKeyStroke(MOD_GUI_LEFT , KEY_R);
    		DigiKeyboard.print('https://www.youtube.com/watch?v=OsY32K1s51Y');
    		DigiKeyboard.sendKeyStroke(KEY_ENTER);

	}
