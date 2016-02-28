# ctf.pragyan.org: Decipher Me

**Category:** Cryptography
**Points:** 100
**Description:**

> Ten years after the starship Voyager's return from the Delta Quadrant, the Federation is in a crisis. The Federation's main suppliers of dilithium crystals (the primary catalyst for the fuel used in faster-than-light travel) are disappearing. Space and time have folded around several planets, isolating them from outside contact. The phenomenon is unnatural – someone or something is causing it to happen. And all they've got is this file. Can you help the Federation ? 

## Write-up

_This writeup was made by stmerry of the [overflow.army](https://overflow.army/) CTF team._

In this challenge, we only had to change the file signature in a hex editor to PNG:

![capture1](https://i.imgur.com/ZWBT8fu.png)

Then add the *.png extension to the file in order to get the flag:

![capture2](https://i.imgur.com/gRWDKm3.png)

The flag is `cyber_punk`.
