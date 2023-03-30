Wave a flag [10 pts]\
tag: general skills\
desc: Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...\
attachment: warm

![image](https://user-images.githubusercontent.com/87841341/224541193-2168b3db-f69d-48a0-8fa8-f60b4e1d2374.png)\
given this challenge, a file named 'warm' is downloaded, reading the tips shows that this is an executeable but with webshell or terminal, so i open up the terminal and made this file executeable
(to run a program on terminal use the command `./filename` but before that to make a program executeable run the command `chmod +x filename` or `chmod 777 filename`)\
![image](https://user-images.githubusercontent.com/87841341/224541510-d965a8ac-4870-45fa-aab0-b681ee8f5268.png)\
seems like it takes argument -h to see what this program does
![image](https://user-images.githubusercontent.com/87841341/224541563-07aeaa4c-2107-4b22-b316-1d72d98aa106.png)\
so this program takes the argument -h and return the flag nice one

<details>
  <summary>FLAG</summary>
  picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
</details>
