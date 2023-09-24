Magikarp Ground Mission [30 pts] \
tag: General Skills \
desc: Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `b60940ca` \
hints: Finding a cheatsheet for bash would be really helpful!
challenge endpoint: ssh ctf-player@venus.picoctf.net -p 57819

this time, the challange consists of ssh connection, lets try to connect to it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/cd414b83-33cd-499b-a622-8562ec704ebf)

after connecting the desc said to ls once lets try to ls it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/365aac1c-c3d2-4882-941f-fd5724b5dc0f)

looks like 3 flag part, lets just read both of the files

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/bdf394ad-9602-4956-b696-5f670ed528c7)

i got the first flag part, it looks like i need to open the / directory, lets see it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/f93ed7d9-cf0f-4059-bb54-3b5ddbd95a54)

i got the second part, and theres the part 3 flag instruction, lets open it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/9e7f73d6-6540-4fc8-ba11-300a14e8dfba)

it seems like the instruction for the 3rd part is on the home directory just a cd command should change to the home directory

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/23d28876-3f61-45c0-a0a0-4dd5e295ad7f)

now the last flag part

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/09dfcb1d-4f07-4e47-adb9-a89bc96d101e)

the flag are now complete

<details>
  <summary>FLAG</summary>
  picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}
</details>
