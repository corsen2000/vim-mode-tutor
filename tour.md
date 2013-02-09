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

Sample - Use "o" to create a new line and type this sentence.