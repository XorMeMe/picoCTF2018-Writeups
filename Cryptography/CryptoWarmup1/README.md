# picoCTF 2018 - Cryptography - Crypto Warmup 1
>points: 75

## Question
>Crpyto can often be done by hand, here's a message you got from a friend, llkjmlmpadkkc with the key of thisisalilkey. Can you use this table [1] to solve it?. 

## Hints
>(1) Submit your answer in our competition's flag format. For example, if you answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag. 
>
>(2) Please use all caps for the message.

## Solution
We know that our ciphertext is `llkjmlmpadkkc` and the key is `thisisalilkey`.
Also, the table we are given should remind us to [Vigenère cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher).
If we try to decrypt the ciphertext [here](https://cryptii.com/pipes/vigenere-cipher) we get the following:
>secretmessage
>
So the flag is:
>picoCTF{SECRETMESSAGE}

