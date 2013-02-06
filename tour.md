# Welcome To Vim Mode Tutor
There are 2 modes in Vim.  Insert mode is your normal editor.  Command mode is
entered by hitting the escape key.  When in command mode the cursor will change
and many key strokes have new meaning.  The exercises that follow always assume
that you are starting in command mode.  Hit escape at any time to enter command
mode.  Hitting escape when already in command mode will cancel any started 
command and leave you in a fresh command mode.

## Follow the pattern
* h -> left
* j -> down
* k -> up
* l -> right

start                                                  
  o     o o o o o o o o o           o o o o o o o o o  
  o     o               o           o               o  
  o     o o o o o       o           o               o  
  o             o       o           o   o o o o o o o  
  o             o       o           o   o              
  o o o o o o o o       o o o o o o o   o              
                                       End

## Delete the extra letters in the sentence
* x -> delete character at the cursor
* Fix the sentence by deleting characters

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Thhe qquick broown foxx jumpedd ovver thee lazzy ddog..

## Insertion
* i -> start insertion at the cursor location
* Fix the sentence by inserting characters

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Te quic bron fo jumpe oer te azy og.

## Appending
* A -> start insertion at the end of the line
* Finish the sentence

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown

## Deleting words
* dw -> delete the word at the cursor
* Delete the extra works

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick brown fox fox jumped over the the lazy lazy dog.

## Deleting to the end of the line
* d$ -> delete all text that follows the cursor on the current line

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox jumped over the lazy dog. the lazy dog. the lazy.

## Deleting with a command and a motion
* d m
* d is the command
* m is the motion and can be
  * w - until the start of the next word
  * e - until the end of the current word
  * $ - to the end of the line
* all motions can be used without a command to move the cursor

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick brown fox fox jumped over the the lazy lazy dog.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox jumped over the lazy dog. the lazy dog. the lazy.

## Adding a count to a motion
* c d w
* c is the count
* d is the motion, in this case delete
* m is the motion, in this case word
* cdw will delete c number of words

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick quick brown fox jumped over the lazy lazy lazy dog.