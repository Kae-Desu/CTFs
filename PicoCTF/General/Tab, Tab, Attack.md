Tab, Tab, Attack [20 pts] \
tag: General Skills \
desc: Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: Addadshashanammu.zip \
hints: After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
attachment: https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip

given this long named zip, without further ado lets try unzipping this zip

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/92ec357d-8613-4e49-9f1d-8839d6eb2774)

wow, the file are really long, as the name suggest i think this is mostly using tab tab, lets just go to the last directory

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/45217595-f770-41c6-ab8b-6c5d38b360cb)

this only include tab tab until the end and theres a last file, it seems like an executeable, lets try to execute it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/ece21fbc-da91-4df1-aff8-3b35dceef488)

<details>
  <summary>FLAG</summary>
  picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
</details>
