# ctf.pragyan.org: Breaking Bar

**Category:** Miscellaneous
**Points:** 100
**Description:**

> Walter White and Jesse Pinkman.

## Write-up

_This writeup was made by stmerry of the [overflow.army](https://overflow.army/) CTF team._

In this challenge, we are given a small program to run and an additional file containing string data related to the binary.
Running this binary in a debugger, we can quickly identify an argument to run it with:

![capture1](https://i.imgur.com/nHmADWB.png)

Running the program with this argument gives us a binary string:

`00110001 00111000 00110110 00111000 00110001 00111000 00111000 00110000` which translates to `18681880` in ASCII.

We now can look for the cipher hidden in the additional file given to us. Using the numbers `1868` and `1880`, we can locate a small string in the file using the character position number, as it is one long string:

![capture2](https://i.imgur.com/Cfu52vG.png)

Later on in the challenge, a hint was given:

> Hint! "B" -> Bifid -> "J" to "I"
> "A" -> Atbash
> "R" -> Railfence
> Break the BAR!

Meaning it is possible to decipher this string using Railfence -> Atbash -> Bifid.
Using tools we then get the following for each stage:

`c@oz@rs#@nc3d` (Railfence)
`x@la@ih#@mx3w` (Atbash)
`w@nn@be#@ck3r` (Bifid)

The flag is then `w@nn@be#@ck3r`.
