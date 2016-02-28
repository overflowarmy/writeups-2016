# ctf.pragyan.org: Johny

**Category:** Forensics
**Points:** 25
**Description:**

> Bob recently found this old file on his old PC. Help him access it. 

## Write-up

_This writeup was made by stmerry and X of the [overflow.army](https://overflow.army/) CTF team._

In this challenge, we are given a password-protected zip file. The password 'peace' was found relatively easily due to how this word is common.
In the archive is contained a text file with the following content:

`loi wtnk az cyhimzm8kka12mo`.

Assuming we can replace the first three words with `the flag is`, we can then recover the whole flag:

The flag is ``.
