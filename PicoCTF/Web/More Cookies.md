More Cookies [90 pts] \
tag: Web \
desc: I forgot Cookies can Be modified Client-side, so now I decided to encrypt them! http://mercury.picoctf.net:25992/ \
hints:
1. https://en.wikipedia.org/wiki/Homomorphic_encryption
2. The search endpoint is only helpful for telling you if you are admin or not, you won't be able to guess the flag name

given a link, lets visit the pages.

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/b7e9346e-8b96-406e-b514-8ee4686432f9">

theres a bunch of clue already, lets se the cookie as the challenge says "only admin be able to use it"

<img width="777" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/2de05c53-7675-47d9-b812-a4072a5fd3a9">

theres a cookie value in a base64 value, lets try to decode this to see the content

<img width="840" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/ea741c4d-d8e7-4568-aeb5-bfdfa92d080a">

this seems off, lets see for another hint, it says a Homomorphic encryption, and the CBC on the desc is capitalized lets do some CBC attack on it

<details>
  <summary>FLAG</summary>
  flag
</details>
