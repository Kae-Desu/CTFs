Scavenger Hunt [50 pts] \
tag: Web \
desc: There is some interesting information hidden around this site http://mercury.picoctf.net:27278/. Can you find it? \
hints: You should have enough hints to find the files, don't run a brute forcer.

given a link to the chall, lets visit the page.

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/645bdaa9-378a-4300-a287-48ca76eb548d">

the page seems similiar to the previous Insp3ct0r challenge, it says the hint are enough to find the files, what does it mean? first lets try to inspect the html to find something interesting

<img width="502" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/77344581-5750-439a-9242-69cf3211a0df">

found the first part, lets see the CSS and JS if theres a flag somewhere (the method are the same as Insp3ct0r challenge)

<img width="690" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/3781a6a9-324d-4386-8864-141d0c112827">

found the second part, lets see the JS for the last part

<img width="518" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/d0d2b174-6eb9-4bff-bb5b-386ef98a2f17">

ouu this one got a new challenge, now it ask for a file that keep google from indexing, it should refer to the legendary robots.txt, lets just visit it

<img width="553" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/a1fad3e7-15d7-4d8c-8f29-1dba64509c06">

find the third flag, and theres another part of the flag, the clue is this is an apache server, apache server got this distributet configuration files which starts with .filename, and the most popular being the .htacces, lets try to vosot these

<img width="604" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/8fe770fb-9921-4780-9e49-566ef39fff6e">

theres the 4th flag part. it shows the next hints that the developer use Mac and store many stuff, this refer to .DS_Store a file exclusive to mac that store custom attributes of its content

<img width="538" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/bdc4c230-85fb-42eb-a338-93f6018e7eff">

theres the last flag part

<details>
  <summary>FLAG</summary>
  picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}
</details>
