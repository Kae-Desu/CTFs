Insp3ct0r [40 pts] \
tag: Web \
desc: Kishor Balan tipped us off that the following code may need inspection: https://jupiter.challenges.picoctf.org/problem/9670/ (link) or http://jupiter.challenges.picoctf.org:9670 \
hint:
1. How do you inspect web code on a browser?
2. There's 3 parts

we're given a link and theres 3 part, also the challenge ask to inspect the web code, firstly lets visit the pages

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/f32a997f-df6c-4ebf-baa2-853e1132dfef">

theres seem to be 2 button one is "what" and the other is "how", on the "how" pages it shows these

<img width="243" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/00a08069-63ec-48bd-b30c-26c4d117feb2">

it looks like the 3 part to check, lets try inspecting the html, open up the inspector (shortcut is available on Cookies writeup)

<img width="530" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/cf00359b-f501-47c5-b50f-22453fd77429">

found the first flag part in html, next lets try to check the CSS, if you ever confuse of where to find the CSS and JS, it's on the head tag, although sometime JS could be placed on body tag.

<img width="614" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/84a23185-2657-4b10-a5c3-ed9c5dbea550">

from here double click on the file name the href one which is mycss.css and paste it on the end of the link, which make it look like http://example.com:1337/some/directory/mycss.css

<img width="703" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/7cc74f3d-326c-46db-96e1-ec2a86339810">

we found the second plag part, the third flag should be in the JS, since we know the JS file name, lets change the mycss.css from before to myjs.js

<img width="689" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/12559701-2ca6-42be-a1bb-372a74369a42">

now all the 3 part flag is acquired. and thats it

<details>
  <summary>FLAG</summary>
  picoCTF{tru3_d3t3ct1ve_0r_ju5t_lucky?2e7b23e3}
</details>
