Python Wrangling [10 pts]\
tag: general skills\
desc: Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script using this password to get the flag?\
attachment: ende.py, pw.txt, flag.txt.en

![image](https://user-images.githubusercontent.com/87841341/224539988-5080a515-68ca-440f-9d36-c8d178af6438.png)
given this challenge and 3 attachment, the desc mention "Can you run this Python script" which mean i should run this python file
to run a python file in terminal use the command `python filename` and it output as below\
![image](https://user-images.githubusercontent.com/87841341/224540173-abea9e07-1735-40b8-ae5d-e6d1c5f27e5f.png)\
seems like the program ask for a parameter and a file to be passed as an argument, to assume this is a cryptography-like challenge -e should be asking the program to encrypt and -d should ask the program to decode, since the file i want to read is flag.txt.en which mean its is encoded, i will go with -d to decode the file\
![image](https://user-images.githubusercontent.com/87841341/224540314-f74fe42d-99d5-4be5-bb9e-8afc3cf26225.png)\
the program ask for password, good thing the challenge already come with the password, lets read the password\
![image](https://user-images.githubusercontent.com/87841341/224540361-5503458d-f211-43cf-aca8-27f722169084.png)\
i got the password, now to pass it to the program. (humbletips: to copy paste in terminal is close as using ctrl+c ctrl+v but with addition of shift key so its like ctrl+shift+c ctrl+shift+v )\
![image](https://user-images.githubusercontent.com/87841341/224540486-6af5c5c8-918c-4ce0-ae9a-c67108d35c0b.png)\
entering the key to the program return a flag as expected

<details>
  <summary>FLAG</summary>
  picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
</details>

