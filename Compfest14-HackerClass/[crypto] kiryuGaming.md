Kiryu Gaming [500pts]\
tag: forensic, steganography\
desc: Kiryu is trying his new purple gaming lamp in his room. What do you think?\
attachment: chall.png

reading the desc giving a tips that, the color purple is somewhat involved in here, then lets start
1. opening the image shows me this image
![image](https://user-images.githubusercontent.com/87841341/184783397-802a486e-3d1d-4f34-ac71-eb87dc312092.png)
2. there is no need to read the binary or metadata since the challenge itself invole in color, so i run a online photo editor pixlr.com, and start to play with the color and filter
3. firstly i color the photo with rough purple, didn't see much so i start playing with other parameter until i can see barely something (thanks to game brightness setting)
![image](https://user-images.githubusercontent.com/87841341/184783978-2657aee9-2fbe-42d9-9ba6-83557d03019e.png)
see a thing? there is a flag near the door, lemme zoom it in\
![image](https://user-images.githubusercontent.com/87841341/184784027-4db547b5-1d94-4fb3-82e0-d56cbf715356.png)\
there is the "comfest" part
4. i took around 30 minutes in playing around the color setting to achive the most readable form for me and here it is
![image](https://user-images.githubusercontent.com/87841341/184784988-4672c307-8d2a-4006-8e27-6f61147edddb.png)
5. there is the flag\
![image](https://user-images.githubusercontent.com/87841341/184785119-efb891aa-9a55-4a8e-a783-3015bd673c88.png)

FLAG: `COMPFEST14{K1rYU_teCH_tIPs_e7cfef1847}`
