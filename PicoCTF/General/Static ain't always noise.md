Static ain't always noise [20 pts]\
tag: general skills\
desc: Can you look at the data in this binary: static? This BASH script might help!
attachment: https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static

given a binary named `static` and it says that "BASH script might help" lets examine the binary, i start with `file static` to determine the filetype

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/950a3bd2-512a-47c6-aaf5-a489a30878a7)

turns out that this is a 64-bit ELF binary lets try and run it

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/ae28c0ec-1fd2-4582-9525-25108811ec55)

the program exit right after execution, no possible input field or smth could the "static" mean something else?
after i read some writeup out there, theres a linux utilities to read strings from a binary its called `strings`, lets try to use it in this binary, using the command `strings static | grep pico` why using the `grep pico`? because we know that the flag format are `picoCTF{*}`

![image](https://github.com/Kae-Desu/ctfs/assets/87841341/3b0856e6-d849-4f28-9630-5d01cdec83b6)

<details>
  <summary>FLAG</summary>
  picoCTF{d15a5m_t34s3r_f6c48608}
</details>
