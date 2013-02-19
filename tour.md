# Welcome To Vim Mode Tutor
Vim is a powerful and popular editor.  It so popular that many other editors
have a vim mode.  Vim mode is a subset of vim and allows you to integrate the 
power of vim with the abilities of the other editor. This tour teaches you how
to use vim mode and helps you practice using the features of vim that are often
found in the vim mode of other editors.

## 3 modes of vim
* command mode - used to enter commands and navigate within a file
  * escape - enter command mode with the escape key
* insertion mode - used to enter text
  * i - enter insertion mode (from command mode) at the cursor location
  * etc... - there are many other ways to enter insertion mode
* visual mode - used to select text
  * v - enter visual mode
  * movement commands will now select text
  * other commands will oeprate on the selected text
  * new commands will be available in this mode



# Movement (Section 1)

Everything in this section can be done without leaving command mode.  If you
are not in command mode, you can enter it by pressing escape.

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
* H -> top of the screen (high)
* M -> middle of the screen (middle)
* L -> bottom of the screen (low)

Try using these commands to move around the screen.  Keep in mind these commands
move around the current visible screen area, not the file.

## Moving by paragraphs
* { -> move up by paragraphs
* } -> move down by paragraphs

## Moving horizontally
* 0 -> start of the line
* ^ -> first non-blank character of the line
* $ -> last character of the line

Try using these commands on the line below.

    This line will help try out the 0, ^ and $ commands.  

## Moving by words
* w -> move to the beginning of the next word
* W -> move to the beginning of the next word ignoring non-space character

Try moving through this setence and check-out the difference in w and W.

* e -> move to the end of the next word
* E -> move to the end of the next word ignoring non-space character

Try moving through this sentence and check-out the difference in e and E.

* b -> move to the beginning of the previous word
* B -> move to the beginning of the previous word ignoring non space characters

Try moving through this sentence and check-out the difference in b and B.

## Jumping to a specific line in the file
* 1G -> jump to line 1 of the file
* 5G -> jump to line 5 of the file

Practice jumping around various lines of the file

## Jumping to the first line of a file
* gg -> jump to the first line of the file

## Jumping to the last line of a file
* G -> jump to the last line of the file

## Matching pairs
* % -> jumped to the matching character
* works for ) ] }

( Here is a [sample] of {what you can do} )



# Editing (Section 2)

Everything in this section can be done without leaving command mode.  If you
are not in command mode, you can enter it by pressing escape.

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

## Yank and put
* y -> copy from the cursor to the new position given by the next command
  * yw -> copy from the cursor to the beginning of the next word
  * y$ -> copy from the cursor to the end of the line
* p -> put the copied text after the cursor
* P -> put the copied text before the cursor  

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox

## Line operations

Doubling a command will often apply that command to the entire line.

* dd -> deleting a line
* yy -> copy a line

Sample:

This is a 
nice little
paragraph.

Fix Me:

This is a
intruder alert
nice little
intruder alert
paragraph.

Sample:

Three times a line.
Three times a line.
Three times a line.

Fix Me:

Three times a line.


         
Arrange the lines by deleting and putting.

1) First Line
4) Forth Line
2) Second Line
5) Fifth Line
3) Third Line

        

# Entering Insert Mode (Section 3)

## Insertion
* i -> start insertion at the cursor location
* I -> start insertion at the beginning of the line
* Fix the sentence by inserting characters

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Te quic bron fo jumpe oer te azy og.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me -
brown fox jumped over the lazy dog.

## Appending
* a -> start insertion after the cursor location
* A -> start insertion at the end of the line
* Finish the sentence

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The qui bro fo jump ov th la do

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown

## Openening lines
* o -> create a new line below the current and switch to insert mode
* O -> create a new line above the current and switch to insert mode

Type the sentence between the examples.

Sample -
The quick brown fox jumped over the lazy dog.
Sample -
The quick brown fox jumped over the lazy dog.

## Replace
* rx -> replace the character at the cursor with x

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Tha qubck brlwn fdx eumped fver thg hazy dig.

## Change
* ce -> change until the end of the word
* works with other motions as well

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - Tha quiaa brola faa jumpaa ovaa taa laaa doaa



# Visual Mode
* v -> enter visual mode which allows selection

## Basic selection
* use any movement key to select the needed text
* y -> copy the selection with the yank command
* p -> paste the selection with the put command 

Sample - The word is repeated 3 times times times
Fix Me - The word is repeated 3 times

## Word selection
* iw -> inner word
* aw -> the word such that a deletion will result in a single space between
* iW -> inner word including any non-space character
* aW -> the word including any non-space character such that a deletion will
        result in a single space between

This is a regular sentence, but it has some style.

## Pair selection
* i{ -> selects everything between 2 matching braces
* i} -> selects anything between 2 matching braces
* i" -> selects anything between 2 matching quotes
* this pattern can be applied to any pair

* a{ -> selects anything between 2 matching braces including the braces
* this pattern can be applied to any pair

{
  try it and see
}

" and it works with quotes as well "



# Enhancing Commands

## Adding a count to a motion
* c d w
* c is the count
* d is the motion, in this case delete
* m is the motion, in this case word
* cdw will delete c number of words
* this pattern can be applied to many commands

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick quick quick brown fox jumped over the lazy lazy lazy dog.

# Extra commands

There commands are not needed because your editor will have its own shortcuts
but it may be easier to use the vim mode shortcut instead.

## Undo

* u -> undo the last action
* usually just an alias to the editors basic undo command

Fix the sentence and then undo it.

Sample - The quick brown fox jumped over the lazy dog.
Fix Me - The quick brown fox jumped over the lazy 

## Bookmarks

* ma -> create a bookmark 'a'
* any single number or letter can be used
* 'a -> return to the line where bookmark a is
* `a -> return to the exact position where bookmark a is

Pratice placing some bookmarks around this file.