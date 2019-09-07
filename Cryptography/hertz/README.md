# picoCTF 2018 - Cryptography - hertz
>points: 150

## Question
>Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with nc 2018shell.picoctf.com 43324.

## Hints
>Here's another simple cipher for you where we made a bunch of substitutions. Can you decrypt it? Connect with nc 2018shell.picoctf.com 43324. 

## Solution
Every time we connect to `2018shell.picoctf.com 43324` we obtain different ciphertext.
Since the name of the challenge is [hertz](https://en.wikipedia.org/wiki/Heinrich_Hertz), maybe with a [frequency analysis](https://www.dcode.fr/frequency-analysis). Alternatively, we can go [here](substitution_ciphers_are_solvable_redpfyedcr) and quickly get the plaintext:
>-------------------------------------------------------------------------------  
congrats here is your flag - substitution_ciphers_are_solvable_redpfyedcr   -------------------------------------------------------------------------------  
"well, prince, so genoa and lucca are now ?ust family estates of the buonapartes. but i warn you, if you dont  tell me that this means war, if you still try to defend the infamies and horrors perpetrated by that  antichrist-i really believe he is antichrist-i will have nothing more to do with you and you are no longer my   friend, no longer my 'faithful slave,' as you call yourself! but how do you do? i see i have frightened you-sit  down and tell me all the news." it was in ?uly, 1805, and the spea?er was the well-?nown anna pavlovna scherer,  maid of honor and favorite of the empress marya fedorovna. with these words she greeted prince vasili ?uragin, a  man of high ran? and importance, who was the first to arrive at her reception. anna pvlovna had had a cough   for some days. she was, as she said, suffering from la grippe; grippe being then a new word in st. petersburg,   used only by the elite. all her invitations without exception, written in french, and delivered by a   scarlet-liveried footman that morning, ran as follows: "if you have nothing better to do, count (or prince),  and  if the prospect of spending an evening with a poor invalid is not too terrible, i shall be very charmed   to   see you tonight between 7 and 10 annette scherer." "heavens! what a virulent attac?!" replied the prince,   not in the least disconcerted by this reception. he had ?ust entered, wearing an embroidered court uniform,  ?nee  breeches, and shoes, and had stars on his breast and a serene expression on his flat face. he spo?e in  that refined french in which our grandfathers not only spo?e but thought, and with the gentle, patroni?ing  intonation natural to a man of importance who had grown old in society and at court. he went up to anna   pvlovna,  ?issed her hand, presenting to her his bald, scented, and shining head, and complacently seated   himself on the sofa. "first of all, dear friend, tell me how you are. set your friend's mind at rest," said he  without altering his tone, beneath the politeness and affected sympathy of which indifference and even irony   could be discerned.  
>
Hence, the flag is `substitution_ciphers_are_solvable_redpfyedcr`.

