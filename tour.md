# Welcome To Vim Mode Tutor
There are 2 modes in Vim.  Insert mode is your normal editor.  Command mode is
entered by hitting the escape key.  When in command mode the cursor will change
and many key strokes have new meaning.  The exercises that follow always assume
that you are starting in command mode.  Hit escape at any time to enter command
mode.  Hitting escape when already in command mode will cancel any started 
command and leave you in a fresh command mode.

# Movement

## Basic movement
* h -> left
* j -> down
* k -> up
* l -> right

Follow the pattern.

start                                                  
  o     o o o o o o o o o           o o o o o o o o o  
  o     o               o           o               o  
  o     o o o o o       o           o               o  
  o             o       o           o   o o o o o o o  
  o             o       o           o   o              
  o o o o o o o o       o o o o o o o   o              
                                       End

## Moving vertically
* H -> top of the screen
* M -> middle of the screen
* L -> bottom of the screen

Try using these commands to move around the screen.  Keep in mind these commands
move around the current visible screen area, not the file.

## Moving horizontally
* 0 -> start of the line
* ^ -> first none blank character of the line
* $ -> last character of the line

Try using these commands on the line below.

    This line will help try out the 0, ^ and $ commands.  

## Moving by words
* w -> move to the beginning of the next word
* W -> move to the beginning of the next word ignoring non space character

Try moving through this setence and check-out the difference in w and W.

* e -> move to the end of the next word
* E -> move to the end of the next word ignoring non space character

Try moving through this sentence and check-out the difference in e and E.

* b -> move to the beginning of the previous word
* B -> move to the beginning of the previous word ignoring non space characters

# Editing

## Character deletion
* x -> delete character at the cursor
* X -> delete the character before the cursor (backspace)
* Fix the sentence by deleting characters

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Thhe qquick broown foxx jumpedd ovver thee lazzy ddog..

## Deletion
* d -> delete from the cursor to the new position given by the next command
  * dw -> delete from the cursor to the beginning of the next word
  * de -> delete from the cursor to the end of the next word
  * d$ -> delete from the cursor to the end of the line
  * etc...
* Delete the extra works

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick brown fox fox jumped over the the lazy lazy dog.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox jumped over the lazy dog. the lazy dog. the lazy.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick brown fox fox jumped over the the lazy lazy dog.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox jumped over the lazy dog. the lazy dog. the lazy.

## Yank
* y -> copy from the cursor to the new position given by the next command
  * yw -> copy from the cursor to the beginning of the next word
  * y$ -> copy from the cursor to the end of the line

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox

## Line operations

Doubling a command will often apply that command to the entire line.

* dd -> deleting a line
* yy -> copy a line

## Insertion
* i -> start insertion at the cursor location
* I -> start insertion at the beginning of the line
* Fix the sentence by inserting characters

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Te quic bron fo jumpe oer te azy og.

Fix the end of the follow line first, then the beginning.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me -
brown fox jumped over

## Appending
* a -> start insertion after the cursor location
* A -> start insertion at the end of the line
* Finish the sentence

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The qui bro fo jump ov th la do

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown

## Adding a count to a motion
* c d w
* c is the count
* d is the motion, in this case delete
* m is the motion, in this case word
* cdw will delete c number of words

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick quick brown fox jumped over the lazy lazy lazy dog.

## Deleting a line
* dd -> delete a line

Sample - This is a 
         nice little
         paragraph.

Fix Me - This is a
         intruder alert
         nice little
         intruder alert
         paragraph.

## Jumping to a specific line in the file
* 1G -> jump to line 1 of the file
* 5G -> jump to line 5 of the file

Practice jumping around various lines of the file

## Jumping to the first line of a file
* gg -> jump to the first line of the file

## Jumping to the last line of a file
* G -> jump to the last line of the file 

## Put
* p -> put copied text at the cursor location
* np -> put copied text n times at the cursor location
* dd -> deleting a line copies the text such that it can be put

Arrange the lines by deleting and putting.

1) First Line
4) Forth Line
2) Second Line
5) Fifth Line
3) Third Line

## Replace
* rx -> replace the character at the cursor with x

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Tha qubck brcwn fdx eumped fver thg hazy dig.

## Change
* ce -> change until the end of the word
* works with other motions as well

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Tha quiaa browa faa jumpaa ovaa taa laaa doaa

## Matching pairs
* % -> jumped to the matching character
* works for ) ] }

( Here is a [sample] of {what you can do} )

## Visual mode
* v -> enter visual mode which allows selection
* y -> copy the selected text
* p -> put copied text

Sample - The word is repeated 3 times times times
Fix Me - The word is repeated 3 times

## Open
* o -> create a new line below the current and switch to insert mode

Type the sentence between the examples.

Sample -
The quick brown fox jumped over the lazy dog.
Sample -
The quick brown fox jumped over the lazy dog.