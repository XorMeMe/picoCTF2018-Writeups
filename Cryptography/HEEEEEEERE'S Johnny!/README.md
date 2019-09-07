# picoCTF 2018 - Cryptography - HEEEEEEERE'S Johnny!
>points: 100

## Question
>Okay, so we found some important looking files on a linux computer. Maybe they can be used to get a password to the process. Connect with nc 2018shell.picoctf.com 38860. Files can be found here: passwd [1]  shadow [2] .

## Hints
>(1) If at first you don't succeed, try, try again. And again. And again. (2) If you're not careful these kind of problems can really "rockyou".

## Solution
We start by typing `nc 2018shell.picoctf.com 38860` in the console:
>Username:
>
We are asked for a username. 
If we a take a look in the passwd and shadow files we see that we have an encrypted password for the root user, which is most likely our target, so let's just type in `root` and press Enter.
>Password:
>
We are now asked for a password.
The name of the challenge is `HEEEEEEERE'S Johnny`. Casually, John is also the name of a linux tool that lets us find weak passwords! 
We first have to generarte a suitable passwd file for John by typing in the console:
>unshadow files/passwd files/shadow > files\ourPasswd
>
Now we can use John:
>john -show files/ourPasswd
>
As a result, we get:
>0 password hashes cracked, 1 left
>
We have an hint! We should try to put `rockyou` and see what happens. Lets do it by typing:
>echo rockyou > files/wordlist.txt
>
Now we can reuse John with our worldlist:
>john -show files/ourPasswd
>
We now get the following output:
>Warning: detected hash type "sha512crypt", but the string is also recognized as "HMAC-SHA256"  
>Use the "--format=HMAC-SHA256" option to force loading these as that type instead  
>Warning: detected hash type "sha512crypt", but the string is also recognized as "sha512crypt-opencl"  
>Use the "--format=sha512crypt-opencl" option to force loading these as that type instead  
>Using default input encoding: UTF-8  
>Loaded 1 password hash (sha512crypt, crypt(3) $6$ [SHA512 128/128 SSE2 2x])  
>Will run 4 OpenMP threads  
>Press 'q' or Ctrl-C to abort, almost any other key for status  
>password1        (root)  
>1g 0:00:00:02 DONE (2019-09-07 11:33) 0.4807g/s 984.6p/s 984.6c/s 984.6C/s 123456..222222  
>Use the "--show" option to display all of the cracked passwords reliably  
>Session completed  
>
As we can see, the password for the root user is `password1`. Now we have to log in with the right credentials using netcat:
>nc 2018shell.picoctf.com 38860  
>Username: root  
>Password: password1  
>picoCTF{J0hn_1$_R1pp3d_4e5aa29e}  
>
The flag is `picoCTF{J0hn_1$_R1pp3d_4e5aa29e}`!
