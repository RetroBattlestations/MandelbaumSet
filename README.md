This is the program for the **eleventh** RetroBattlestations BASIC
challenge. 

It seems like fractals have become popular again, so I present to you
*The Mandelbaum Set*.

This program will iterate over and over chanting along, generating
smaller and smaller chants using matrix transformations. While
Applesoft supports using 2D arrays, not all BASIC dialects do and
since the matrix is only 3x3 I simulated a 2D array using very simple
math (mathsfsh for you British people). Like any good fractal
rendering program, it's very slow. You're also going to want a decent
resolution - character block graphics really isn't going to cut it. In
fact outputting to a pen plotter may give some nice results, if you're
up to rewriting the program to do it!

Since this uses techniques I've never used before - namely matrix math
- I chose to write the program in Python and get it working there
first, and then convert the program to BASIC. Keeping track of 2
letter global variables in BASIC was more challenging than
usual. Having to deal with line numbers also provided some additional
challenges. And of course there were the usual simple mistakes during
translation such as typos and forgetting about managing all my loops
myself. But overall I think making the program work in Python first
probably was the way to go. (Someone should write a Python to BASIC
compiler!)

As always, I did my best to write the subroutines in a way that they
might be reusable as some sort of "library" for other programs you may
decide you want to create.

For more details about the challenge, check out the post here:

  https://redd.it/oevqbq

## Porting ##

Before you start working on porting the program and changing things to
work on your machine, try running the Apple II version in an emulator
(or real hardware if you are so inclined) so you can see how the
program works and what it does. The advantage of testing in an
emulator is that many emulators will allow you to easily paste text as
if it were keyboard input so you don't need to hassle with manually
typing it in or figure out how to convert the listing to a tape or disk image.

See [List of Computers With On-Board BASIC](https://en.wikipedia.org/wiki/List_of_Computers_With_On-Board_BASIC)

## Enhancment Ideas ##

* Send output to an external high resolution device
* Turn it into some kind of continuously looping animation
* Reduce the number of redundant calculations and make it run faster

## Typing Tips ##

When typing the program in you can leave off any lines which begin
with REM, they are not needed for the program to run. On many
platforms you can leave out the whitespace between keywords and
operators. IBM BASIC is not one of those however.

*Note*: On the TRS-80 Color Computer and BBC Micro you need to include
      the spaces around any IF, AND, OR, or THEN statement.

If you make a mistake and don't want to retype the entire line, most
of the BASICs have a way to make corrections.

### Amstrad CPC (464/664/6128/464+/6128+) ###

  On Amstrad CPC, use AUTO to start typing commands. Use the arrow keys
  to move about the line. Exit the AUTO mode py pressing Escape. You can
  also start on a specific line by entering AUTO 100 (for line 100).

  To go to the start or the end of the line use CONTROL+Arrow keys. You
  can also use SHIFT+Arrow keys to use the copy cursor. This is a second
  cursor that you move independendly, and will copy whatever is under it
  to the main cursor when you press COPY.

### Apple II computers ###

  On an Apple II+ use LIST <line number> to print the line with an
  error, then use ESC followed by A/B/C/D to move the cursor one step
  at a time. Position the cursor at the beginning of the line, then
  use the right arrow to move over the line and fix the error. Be sure
  to arrow all the way to the end of the entire line before you hit
  RETURN!

  On an enhanced Apple IIe, Apple IIc, or Apple IIgs you can also use
  ESC with the arrow keys. In 80 column mode (enter with PR#3) the
  cursor will change to a white block with a + in it, push ESC to drop
  out of movement mode.

### BBC Micro ###

  Use LIST <line number> to print the line with a mistake, then use
  the arrow keys to move up to the beginning of the line. Each press
  of the copy key will type in the character under the cursor. Make
  any necessary edits by just typing on the keyboard and using copy to
  avoid retyping everything.

### Commodore 64, Plus/4, and 128 ###

  Like the others, use LIST <line number> to display the line with
  problems, then use the arrow keys to move up and make any
  corrections. By pressing shift-INST you can insert a blank character
  if you missed something. Unlike the Apple II you don't need to arrow
  to the end of the line before pushing RETURN.

### IBM Cassette BASIC, Disk BASIC, Advanced BASIC, GW-BASIC ###

  Type EDIT <line number> and it will print the line on the screen and
  put your cursor at the beginning of the line. Arrow left/right and
  you can use Insert & Delete to make corrections. Like Commodore
  BASIC, you don't need to arrow to the end of the line before pushing
  RETURN.

### TI-99/4A Extended BASIC ###

  Type the line number and then arrow up (FCTN+E) and it will enter
  edit mode with that line loaded.  You can move within the line with
  arrow left (FCTN+S) and arrow right (FCTN+D) and move to the
  previous or next line with arrow up (FCTN+E) or arrow down (FCTN+X).
  You can delete the character under the cursor with DEL (FCTN+1) or
  turn on insert mode to insert extra characters with INS (FCTN+2).
  You do not need to move to the end of the line before pressing
  ENTER.

### TRS-80 model 100 ###

  This has to be the best built-in BASIC editor I've seen so far! Just
  type EDIT and the entire BASIC program will be loaded into the
  built-in word processor where you can make any changes you
  want. Press F8 to exit the editor and go back to BASIC.

### ZX81, Timex-Sinclair 1000, and ZX Spectrum ###

  Having a hard time finding where all the BASIC keywords are hidden?
  Get [Commander le Clef's Secret Encoder
  Wheel](http://retrobattlestations.com/Cmdr-le-Clef/Secret-Encoder-Wheel.pdf)
  with an alphabetical sorted listing of keywords and the secret
  keypresses required to enter them.
