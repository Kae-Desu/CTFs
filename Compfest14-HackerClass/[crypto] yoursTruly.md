Yours Truly [500 pts]\
tag: cryptography, rsa\
attachment: chall.zip\
desc: I want to send this message to my friend Alice but I'm too busy. Can you send it to her? It has sensitive information though, I've protected it using Alice's RSA public key so don't bother peeking!

this challenge is obviously a rsa encryption, and encrypted with public key, so assuming i have to recover the private key from the public key then.

1. given the chall.zip, extract the files with `unzip chall.zip` and given 2 files: message.enc, publickey.pem
![image](https://user-images.githubusercontent.com/87841341/184668662-a0ae146f-114c-4b42-8c7f-bafbadde309a.png)
2. using `cat` command at the 2 files gives out garbled on message.enc and of course the rsa key on the publickey.pem
![image](https://user-images.githubusercontent.com/87841341/184669381-ceebb219-4fe3-4f2d-a3fc-a6f254f24d0b.png)
3. using the command `python` i entered python environment and start to importing modules\
 `from Crypto.PublicKey import RSA`\
  `from Crypto.Util.number import bytes_to_long`\
  `from Crypto.Util.number import long_to_bytes`\
  `import math`
4. then the real challanges start here, we know that pubkey is made of modulo n and e, so using this command to read the pubkey
  `pubkey = RSA.importKey(open("pubkey.pem", "r").read())`
5. then print out the n and e using `print(pubkey.n, pubkey.e)` gives out
![image](https://user-images.githubusercontent.com/87841341/184671271-4f5cb4ab-6fc0-42d5-85a4-648eac2207bc.png)
6. given big chunk of n, i tried using the factordb and gives out so much factor
![image](https://user-images.githubusercontent.com/87841341/184671553-5cfaf22c-9b3f-4931-9b85-469f47ef4b49.png)
7. long story short, i copy all of them regex to remove so only the digit 1 need seperated with coma and insert them to variable names `factors`\
![image](https://user-images.githubusercontent.com/87841341/184671792-4d353cc4-6a0b-4187-b7bb-8f0717961603.png)
8. then to find the phi, using the command `phi = math.prod([i - 1 for i in factors])` to find all the phi in the factors, and turn out to be
![image](https://user-images.githubusercontent.com/87841341/184672023-c7d21f8a-f519-48b6-adb2-07f75d2b827a.png)
9. preparation was ready, and i want to start working on the message, since it's a garbled text, i think to it's possible to read in binary mode and convert it to long, so i add this command
  `c = bytes_to_long(open("message.enc", "rb").read())`
10. then the d \
  `d = pow(pubkey.e, -1, phi)`
11. the flag \
  `flag = pow(c, d, pubkey.n)` 
12. and it works, but when i print out the flag, it's still in random numbers
![image](https://user-images.githubusercontent.com/87841341/184672879-e284369b-4290-4b54-975c-84ea0018033e.png)
13. to turns it out into it's ascii form, use the `long_to_bytes` command, and it gives out the flag
![image](https://user-images.githubusercontent.com/87841341/184673159-13956240-0e6c-4277-9f65-73416537491d.png)

there it is the flag
FLAG: `COMPFEST14{hello__how_are_you_?_i_hope_youre_doing_alright_thank_you_and_good_bye_2fdf9d6610}`
