# picoCTF 2018 - Cryptography - Crypto Warmup 2
>points: 75

## Question
>Cryptography doesn't have to be complicated, have you ever heard of something called rot13? cvpbPGS{guvf_vf_pelcgb!}

## Hints
>(1) This can be solved online if you don't want to do it by hand!

## Solution
We know that our ciphertext is `cvpbPGS{guvf_vf_pelcgb!}` and `rot13` should immediately remind us to [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher).
If we try to decrypt it [here](https://cryptii.com/pipes/caesar-cipher) with a shift of `13` we get the following:
>picoCTF{this_is_crypto!}
>
That is the flag!
