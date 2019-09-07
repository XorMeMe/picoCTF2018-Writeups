# picoCTF 2018 - Cryptography - caesar cipher
>points: 150

## Question
>This is one of the older ciphers in the books, can you decrypt the message [1] ? You can find the ciphertext in /problems/caesar-cipher-1_3_160978e2a142244574bd048623dba1ed on the shell server.

## Hints
>(1) caesar cipher tutorial [2] 

## Solution
If we open the `ciphertext` file we see:
>picoCTF{grpqxdllaliazxbpxozfmebotlvlicmr}
>
Unfortunately, this isn't the flag.
We know it's encrypted with caesar cipher. If we try to decrypt it [here](https://cryptii.com/pipes/caesar-cipher), we can see that with a shift of 23 we get:
> justagoodoldcaesarcipherwoyolfpu
>
So, the flag is `picoCTF{justagoodoldcaesarcipherwoyolfpu}`.
