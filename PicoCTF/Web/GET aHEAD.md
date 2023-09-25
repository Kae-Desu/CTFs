GET aHEAD: [20 pts] \
tag: Web \
desc: Find the flag being held on this server to get ahead of the competition http://mercury.picoctf.net:53554/ \
hints: 
1. Maybe you have more than 2 choices
2. Check out tools like Burpsuite to modify your requests and look at the responses

given a web challenges, lets try to visit it first

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/7664824a-5158-42b5-98c6-6b1808152099">

seems like theres only 2 button to change the background color, but the title kinda gives a hint to GET a HEAD, i should try to do a HEAD request to the web using curlwith this command `curl -I HEAD http://mercury.picoctf.net:53554/`

<img width="501" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/8d6e71a6-4145-4a12-9a3b-41ba6d4f1703">

theres the flag

<details>
  <summary>FLAG</summary>
  picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
</details>
