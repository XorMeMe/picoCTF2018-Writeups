# picoCTF 2018 - Cryptography - blaise's cipher
>points: 200

## Question
>My buddy Blaise told me he learned about this cool cipher invented by a guy also named Blaise! Can you figure out what it says? Connect with nc 2018shell.picoctf.com 26039.

## Hints
>(1)There are tools that make this easy. 
>
>(2) This cipher was NOT invented by Pascal.

## Solution
We firstly have to type in the terminal:
>nc 2018shell.picoctf.com 26039
>

We can see an encrypted message (files/ciphertext.txt).
Well, Blaise is the first name of Vigenère, maybe we have to use his cipher.
If we go [here](https://www.dcode.fr/vigenere-cipher) we can decrypt the message by guessing the key size. With a key size equals to 4, we get the right plain text (files/plaintext.txt), and also the flag:
>picoCTF{v1gn3r3_c1ph3rs_ar3n7_bad_901e13a1}
