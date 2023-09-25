Cookies [40 pts] \
tag: Web \
desc: Who doesn't love cookies? Try to figure out the best one. http://mercury.picoctf.net:6418/ \

given the web challenge, lets firstly try to visit the pages

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/2c3f0b70-e3db-433a-8b70-dcc225876a91">

the descripion and title says about cookies, this actually contain cookies for the webpages, open up inspect (ctrl + shift + i on windows, linux or command + option + i on mac) and open the cookie tab (application > cookie on chrome. or storage > cookie on firefox)

<img width="1176" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/cc1bf192-9ed0-4a07-a343-5e14422f1043">

the cookie currently being set to -1 lets try to input something and see what is the response, lets try "ginger bread"

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/ea0dd4e3-4030-4b63-b63f-c9602773ab3a">

the value change to 23, what if i put something non existent cookie like "this is not a cookie"

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/2832beee-457d-4052-9073-f2e55f7bc45d">

seems like it goes back to -1 and says that it is not a cookie, since different cookie change the cookie value, lets try to change it from -1 to 0..n, which mean we brute force all the possible cookie, pls remember to reload the page everytime we change the cookie
(i prefer to do it with burpsuite, but since this is for a learning purposes and still could be solved manually, lets try to solve it manually)

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/751493d1-9851-4bb5-98da-445f5c50447a">

after changing the cookie to 0 notice that the content change to "snickerdoodle", lets repeat the process until i found the flag

<img width="1792" alt="image" src="https://github.com/Kae-Desu/ctfs/assets/87841341/20e56e4c-80ea-4a5e-be60-212d78fddd2b">

we got flag. the flag is in the cookie 18

<details>
  <summary>FLAG</summary>
  picoCTF{3v3ry1_l0v3s_c00k135_88acab36}
</details>
