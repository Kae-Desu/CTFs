Some Assembly Required 1 [70 pts] \
tag: Web \
desc: http://mercury.picoctf.net:1896/index.html \

given a link, lets visit the sites

<img width="540" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/ddd6acea-98c0-4721-b34f-c6995e348225">

looks like a flag checking tab, lets check for another stuff such as JS or CSS

<img width="966" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/9bd8e24e-4653-4373-a0dc-667a70a0dbec">

found the source code, lets try to find something interesting

<img width="165" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/b2f4039e-a4cd-4497-ab3f-6942cb383fc2">

notice on line starts with "./" in line 14 its a file named 'JIFxzHyW8W', lets visit it

<img width="173" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/a8a47229-7c48-4ccd-bfed-b2887847c342">

i downloaded a file named "JIFxzHyW8W"

lets open it

<img width="794" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/cccd8621-d779-4c66-b5bf-0757dc1003ad">

notice theres a flag in the bottom, thats the flag, use the command `strings filename`, so it doesnt get problem

<details>
  <summary>FLAG</summary>
  picoCTF{a2843c6ba4157dc1bc052818a6242c3f}
</details>
