# Dial-O-Tron
A nostalgic, procedurally-generated hacker adventure played 7 digits at a time.

[Try it at my CodePen](https://codepen.io/Unhacker/full/VwowxWL)!

Disclaimer: I know *nothing* about game design; I made this because I enjoy writing weird code.

This repository exists to document how it works before I forget. Code here may lag behind [CodePen](https://codepen.io/Unhacker/full/VwowxWL).

# Excerpt from 'Projects' entry: 

It's like [Doors](https://github.com/diemastermonkey/doors), but instead of a maze it's a local area code full of phone numbers. The user interface is (some sort of) phone, with DTMF dialing and old-school phreaking stuff. Discover and interact with NPCs, voicemail, control systems, dead-drops. Collect clues, solve puzzles, acquire mods, gain access - retake the network for the people! Since you've come this far, you can peek at one of its [secret artifacts!](https://pastebin.com/raw/sudbDdHF)

Ultimately, I will wrap this and get it onto Android for the Play store.

# Gameplay Synopsis
How gameplay works. Theoretically. 
If you're really more curious about the game aspect, check out 'Lore', below.

# Concepts 
(Key concepts needed to understand wtf is going on.)
Everything starts when a user enters a 7-digit number. The number is used 

## Procedural Generation
Most randomization you'll see in Javascript will use `Math.random`, which returns a 'random' value each time it's called. 

These values should be difficult to predict; That is the closest any deterministic system like a computer can get to 'truly random'. Yes, I will happily argue this with you in the comments.

But for Dial-O-Tron, we need an algorithm that produces *seemingly* random results that actually are completely consistent for a set of given inputs. For example, `SpecialRand(123)` would return output 'K' every time, yet it would remain difficult to predict in advance what `SpecialRand(456)` would return.

This, in a nutshell, is Procedural Generation on-the-cheap.

This could be accomplished with many algorithms, such as the Perlin Noise I use my unpublicized 'Entroscope' app for Android. In that, geolocation and clock data are inputs to generate game data on-the-fly, according to the results of a Perlin Noise function.

In Dial-O-Tron, the entire mathematical domain of possible inputs is much smaller: Only 'possible local phone numbers', so 10^7 (10,000,000). Maybe that seems alot, but for an entire universe it's tiny. 

A popular, computationally cheap algorithm will suffice as a "seedable" Random Number Generator. (link to the function)

For each NPC (or other procedurally-generated entity), the 'phone number' is used as the seed. Instantiated with that seed at runtime, our custom 'non-random random number generator' produces the necessary illusion of 'consistent diversity'.

(to do: add code snippets and links to relevant sections)

## Tokenization
Tokens are in everything. Omg there are so many tokens now.

## Self-Modifying Runtime Code 
So much self-modifying code I'm no longer sure if I'm writing this, or it's writing itself.

# Gameplay Engine
How game state and player workflow is handled. 

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

# Lore
You can tell I'm not a gamer because this is last. However, I *am* an artist - so 
you may be surprised by how much story and lore I have baked-in, and how elaborate 
some of it is. (discuss the premise, game world, and lore here).

