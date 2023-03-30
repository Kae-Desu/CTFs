Unidentified Transmission [500pts]\
tag: forensic, pcap\
desc: I heard some eerie noises when I was streaming. I wonder what it is\
attachment: transmission.tar.xz

reading the tag allows me to identified that the file is a pcap, and it's an audio file to recover.

1. i start by extracting the attachment by using `tar -xf transmission.tar.xz` and it's true i was given a `transmission.pcap`
![image](https://user-images.githubusercontent.com/87841341/184785999-74e6c221-40de-451c-a0eb-93650d5d7409.png)
2. since it's a pcap, i tried to open the file with `wireshark trasmission.pcap` and it shows this
![image](https://user-images.githubusercontent.com/87841341/184786134-60e26325-48bb-408d-a344-6f69c30c8be3.png)
3. so many udp packets, and since it's an audio files, i might want to decode the packet as RTP and it shows this
![image](https://user-images.githubusercontent.com/87841341/184786347-fc24c60c-ef06-4be6-a689-08fabf81c268.png)
4. yes its an uncompressed audio file, then i proceed to rtp stream and it shows this audio
![image](https://user-images.githubusercontent.com/87841341/184786652-40525b8b-badf-4242-966f-761b91fdd020.png)
5. the audio is very loud and uncomfortable to hear, what to do with this audio? reading it with spectogram? ctf challenge wont use same trick twice.. since it's a transmission it might be something else, maybe it's a video or an image, i start researching about signal converter to an image or video and found an apps name robot36\
   this apps able to turn audio to an static image (sstv i searched) and start playing the audio.
![image](https://user-images.githubusercontent.com/87841341/184787176-0e473a2e-1a51-4458-9713-8e24dbcd74d5.png)
6. given qr code, i scan with phone and was given the flag\
![image](https://user-images.githubusercontent.com/87841341/184787366-3de17b13-38df-401a-b25e-1d6ba97da1a2.png)

FLAG: `COMPFEST14{1t_w4s_1nde3d_4n_1ma9e_tr4nsmiss1on_huh_019d8ec6f6}`
