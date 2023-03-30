Naik Pangkat [500pts]\
tag: forensics, steganography\
attachment: Hmm.zip\
desc: Pak Josefumi, kepala divisi File Forensic, memberi Title pada nama setiap anggota divisinya agar dapat memotivasi anggota-anggota di dalam divisi. Title tersebut menggambarkan pencapaian mereka setelah menyelesaikan tantangan sulit dari Pak Josefumi, yang mana hanya diadakan tiga bulan sekali. Tertarik untuk mendengar panggilan namamu diikuti oleh Title tersebut setiap kali dipanggil oleh teman-temanmu, kamu menerima tantangan pada hari itu.

1. in this challenge i have no idea or clue from the title or even the desc, so i run terminal `unzip Hmm.zip` and given `Hmm.jpeg`
![image](https://user-images.githubusercontent.com/87841341/184775879-87eef51d-320f-4df7-a651-40925e4b9384.png)
2. an image? wow that's easy.. opening the image given an output like this\
  `the image Hmm.jpeg cannot be displayed because it contains errors.`
3. honestly i will be much shocked if it's not an error, so what might causes a file to be error? `corrupted file`and `bad or wrong header`, so i took a peek with hexedit to see if there is something.. and there is something
![image](https://user-images.githubusercontent.com/87841341/184778862-6ec8fc46-9800-4edc-bbc7-24b632a24103.png)
4. yep the header is not an jpeg, it's an audio files (.wav), simply rename the files and successfully played the files
![image](https://user-images.githubusercontent.com/87841341/184779301-4513848f-fb58-428e-b0a2-88726d3b1caf.png)
5. but the audio is somewhat garbled, no voice only random robotic noise, what could it be... i think a bit and remember that sound has a graph representation name spectograph or spectogram i think, so i download sonic visualiser (audacity and any other daw work great), opening the files with sonic and change it to spectogram view shows this\
![image](https://user-images.githubusercontent.com/87841341/184780209-42c6962f-4d78-4e41-9c5b-cfa1dfec299b.png)
6. looks 'flag-ish' to me, luckily sonic has a zoom vertically and horizontaly seperated, so adjust until i can see it clearly and..
![image](https://user-images.githubusercontent.com/87841341/184780597-9e15e42a-7a43-4338-802a-9ec7378899e6.png)
7. it's a flag, good game btw

FLAG: `COMPFEST14{m4STeR_0f_fil3_STruCtuRe_4nd_aUDi0_aNAlys1S_4185015c52}`
