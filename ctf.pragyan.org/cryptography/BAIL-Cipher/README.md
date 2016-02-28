# ctf.pragyan.org: BAIL Cipher

**Category:** Cryptography
**Points:** 20
**Description:**

> Bob and Alice have come up with a new encryption to communicate. But they want you to figure out if its possible to decipher their messages easily. Can you decipher it?
> VGF4ME9GaGxnIHdXMkZqaDVlZiBzeFFtNHY5IGlsdWI= 

## Write-up

_This writeup was made by stmerry of the [overflow.army](https://overflow.army/) CTF team._

Looking at the cipher text and the name of the challenge, straight away it seems there is a mix of Base64 and Rail cipher in there.

Decoding the base64 string gives us the following:

`Tax0OFhlg wW2Fjh5ef sxQm4v9 ilub`

And decoding this with the Railfence cipher decoder using a rails number of 4 gives us the flag:

The flag is `xwxlQW02mu4FOjvb9hF5`.
