# picoCTF 2018 - Cryptography - caesar cipher 2
>points: 250

## Question
>Can you help us decrypt this message [1] ? We believe it is a form of a caesar cipher. You can find the ciphertext in /problems/caesar-cipher-2_1_ac88f1b12e9dbca252d450d374c4a087 on the shell server.

## Hints
>(1) You'll have figure out the correct alphabet that was used to encrypt the ciphertext from the ascii character set 
>
>(2) <a href="https://www.asciitable.com/">ASCII<a> Table

## Solution
Different alphabets were used so we can simply go [here](https://www.dcode.fr/rot-cipher), insert the ciphertext and get the flag:
>picoCTF{cAesaR_CiPhErS_juST_aREnT_sEcUrE}