# picoCTF 2018 - Cryptography - hertz 2
>points: 200

## Question
>This flag has been encrypted with some kind of cipher, can you decrypt it? Connect with nc 2018shell.picoctf.com 39961.

## Hints
>(1) These kinds of problems are solved with a frequency that merits some analysis.

## Solution
We firstly have to type in the terminal:
>nc 2018shell.picoctf.com 39961
>

We get:
>Let's decode this now!
Hlt fjwbd xcani ras qjkpu amtc hlt vyzg oae. W byi'h xtvwtmt hlwu wu ujbl yi tyug pcaxvtk wi Pwba. Wh'u yvkauh yu wr W uavmto y pcaxvtk yvctyog! Adyg, rwit. Ltct'u hlt rvye: pwbaBHR{ujxuhwhjhwai_bwpltcu_yct_haa_tyug_oieyankmgt}
>

It's a substitution cipher. We can go [here](https://quipqiup.com/), insert the cipherttext and, after a bit of analysis, these clues:
>p=p
i=n
d=k
e=g
f=q
n=w
>

By clicking the solve button, we get the plaintext with the right flag, which is:
>picoCTF{substitution_ciphers_are_too_easy_dngaowmvye}