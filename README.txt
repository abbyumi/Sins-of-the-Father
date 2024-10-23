Project 2 - ink interactive fiction story / game 
Sins of the Father by ABIGAIL SANCHEZ

Word count: About 2,900+ 
This story is an original story that I've personally created. 

You play as a father who struggles from depression due to the death of his loved one. Their death had caused a major emotional imbalance between you and your daughter, 
and tension is only getting worse as weeks passes by. You only have one day to reconnect with your daughter before she leave for university. However, that is only possible 
depending on your actions around the house and the choices you make around your daughter. As you explore through the house, you'll be able to gain more information by 
interacting with the environment. 

--------------------------
Decision point 1: Fix the portrait (choice 1), Take the portrait (choice 2), or continue sleeping (choice 3).
This decision point is heavily important to the player to make because either they can be responsible and fix the portrait of their dead spouse, 
which makes the character confront with the photo and be reminded of the truth. The 2nd choice is the opposite, where the character still lives in denial 
and would rather keep hiding the photo. You would have the option to give away the photo at the end of the game. These choices can be completely ignored 
though if the player chooses to sleep instead. The third choice would be met with a game over.

Can be found in line 19 - 22 
 // Decision 1
 * [Continue sleeping.]-> Sleep
 * [Fix the Portrait.]-> FixedPortrait
 * [Take the Portrait.]-> Takeportrait

Decision point 2: Give Cigarettes to your daughter (choice 1) or Deny and keep your cigarettes (choice 2)
Depending of the player's choices, they'll end up with any of the possible endings. If they were to keep the cigarettes, they'll be met with another set of 
decision to pick from. The player has a chance to continue their story a bit longer, or be met an abrupt bad ending. For more context, the father has an 
smoking addiction and his daughter was the only one who would actively warn him about the dangers of it, even trying to take them away without him knowing. 
Hence why the player would be met with this decision, as the character runs into her daughter while smoking. However, the first choice will allow the player 
to continue the story longer much longer compared to the 2nd choice and have more choices to make before finally reaching to either of the possible endings.

Can be found in line 212 - 214
// ROUTE 2 DECISION 1
 *[Give her your cigarettes.] -> GIVECIGS
 *[Deny and keep your cigarettes.] -> KEEPCIGS

Decision point 3: The player has the option to either pet the dog or use computer. Each choice leads to a different path in the story as one of the choices
reveals more information to the main character. Petting the dog strengthens the character's relationship with their child, while the other choice makes
the main character distance himself from his daughter.

Can be found in line 116 - 118
// ROUTE 1 DECISION 2 
*[Pet dog.] -> PETDOG
*[Use computer.] ->FAMILYCOMP

Decision point 4:The player has the option to either eat the daughter's food or refuse it. Each choice leads to a specific path in the story and effects
the outcome of the daughter's opinion on the father (player).

Can be found in line 169 - 171
// ROUTE 1 DECISION 3
*[Eat her food.] -> EAT
*[Don't eat her food.] ->DONTEAT

--------------------------
Two Endings:

BADENDING2: One of the bad endings to the game. To achieve this ending, the player has to choose a few specific decision points such as the portrait and smoking.
The player would have to pick up the portrait, deny giving away your cigarettes to your child, and remain silent. This is the second shortest ending compared to the 
first one, which can occur at the beginning of the story (if player decides to continue sleeping).

BADENDING3: One of the bad endings to the game: To achieve this ending, it might be considered tricky or unknown compared to other endings. The only way to access it 
is if the player interacts with the family's computer. The player needs to fix the portrait, visit the living room, don't  help her pack, then use the computer rather 
than interacting with the dog. It would then force the player to go outside and proceed with the bad ending. 

--------------------------
Conditionals / conditional choices / variables

First conditional: 
Lines 87 - 90
// Conditionals / Variables
*[Follow her to the kitchen.] -> KITCHEN
+ {KIDSROOM} [Hand over plushie.] -> PLUSHBEAR

Second conditional:
Lines 276 - 279
// Conditionals / Variables
+ { FAMILYCOMP } [ Bid farewell. ] -> BADENDING3
+ { not FAMILYCOMP } [Hand over the portrait.] -> GIVEPHOTO
+ { not FAMILYCOMP } [Keep the portrait.] -> KEEPPHOTO

 --------------------------
HTML / CSS changes

First change: Changed the background from white to black 
Line 2: #theme:dark
Second change: Changed the font for some headers + text. It was fully in roman font before I've decided to change it to poppins.
Line 1 and 31-33 (CSS)
Third change: The default color for options was yellow . I've changed it to a purple color.
Line 225 - 275 (CSS - color: #99447f)