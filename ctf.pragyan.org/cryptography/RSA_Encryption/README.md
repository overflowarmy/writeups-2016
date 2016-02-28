# ctf.pragyan.org: RSA_Encryption

**Category:** Cryptography
**Points:** 25
**Description:**

> X has sent a message. Can you decrypt it?
> The encrypted message and the public key used to encrypt it ( key1_data.txt ) are given to you. 

## Write-up

_This writeup was made by stmerry of the [overflow.army](https://overflow.army/) CTF team._

In this challenge, we are given a *.tgz file which we can extract to get the following files:

- ciphertext.txt (the cipher text in base64 encoded form)
- key1_data.txt (the public key that has been used to encrypt the message, containing the modulus n and exponent e
- key2_data.txt (an additional public key given with no apparent reason, except that...)

In this case, it seems we are being asked to crack 768 bit RSA. The assumption is that we have been given a second public key that has been created using a common p value. If that is the case, we can [use a tool](https://github.com/Rawrz/RSA-Public-Key-Cracking) to retreive both p and q value associated with key1_data.txt.
In turn, we will then be able to generate our d value which will be used to decrypt the encoded message.

Using these techniques, we get the d value based on the information from key1_data.txt:

`fb2f56ba12cb3ef5be86ef481300d5a4289a6c85564319beb79b12917a9689117f2c44912a2ea3980cdb02fa990a3bc22c7c7ade878beba7d6ec66e102ac1d4e1d28f00c1d12fdf9b728459bb1a6970d402ed1d420fc904c5c02b37804eb7a8218248b58830ceb27ef9fbaab8a69b019ba6bce9d6272048b36cf5d37903cf61`

We can then use a python script called [rsatool.py](https://github.com/ius/rsatool/blob/master/rsatool.py) to generate the private key from n, d, and e.

Once done, we can write a quick python script (decrypt.py) to decrypt the message.

The flag is `nothing_is_impossible`.
