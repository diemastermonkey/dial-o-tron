# Dial-O-Tron
A nostalgic, procedurally-generated hacker adventure played 7 digits at a time.

Try it at [my CodePen!](https://codepen.io/Unhacker/full/VwowxWL)

# Excerpt from 'Projects' entry: 

It's like [Doors](https://github.com/diemastermonkey/doors), but instead of a maze it's a local area code full of phone numbers. The user interface is (some sort of) phone, with DTMF dialing and old-school phreaking stuff.

Discover and interact with NPCs, voicemail, control systems, dead-drops. Collect clues, solve puzzles, acquire mods, gain access - retake the network for the people! Since you've come this far, you can peek at one of its [secret artifacts!](https://pastebin.com/raw/sudbDdHF)

Ultimately, I will wrap this and get it onto Android for the Play store.

# Gameplay Synopsis
How gameplay works. Theoretically.

# Concepts 
Key concepts needed to understand wtf is going on.

## Procedural Generation
How ProcGen is used

## Tokenization
Tokens are in everything

## Self-Modifying Runtime Code 
So much self-tweaking code 

# Gameplay Engine
How game state and player workflow is handled

## DOT Object
A class representing the user's fictional device

## NPC Objects
A class representing NPCs procedurally generated on-the-fly
NPCs can implement 'entities' like people, or automated or interactive systems, even system glitches for players to exploit.

## Response Scripts
How both NPCs and the engine itself use response scripts.

## Tokens
How tokens increase the range of ProcGen variability and make more content out of less. 
And they're sometimes used as a workaround or 'trick' in response scripts.

## Inline Commands
How inline commands {in brackets} are used throughout response scripts.
Inline commands use, change, or even create or delete tokens on-the-fly.
How the flow of response script entries is used to execute inline code 
in order when necessary. For example, the 'greeting' response may include 
code that sets variables that code in the 'middle' or 'goodbye' responses 
can reference. This sometimes used to change how a response script behaves 
depending on a check or function performed earlier in the script.



