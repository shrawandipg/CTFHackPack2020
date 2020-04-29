# CTFHackPack2020
Download the file here: [Listen UP!](https://ctf2020.hackpack.club/challenges#Listen%20UP!)

![image](https://user-images.githubusercontent.com/44412255/80644712-1b5b6e80-8a38-11ea-8200-cf9b4baf9fb4.png)

<br>
For solving this level, you can first try to open the file using any editor. Doing so, I got the hint for this level.<br>
After going to the hint, I found out it was a video in youtube that had sound of MSPaint executable file. So, I thought <br>
Listen Up! flac file is also related to the executable.
<br>
While oberving the first few lines of the flac file in editor, I came across readable string saying comment was processed by<br>
SoX so, I investigated how SoX actually work and what it is used for.
<br>
Steps to solve this challenge:
<br>

1. Download the SoX package as: **sudo apt-get install sox**<br>
![1](https://user-images.githubusercontent.com/44412255/80645682-75106880-8a39-11ea-8443-a71248765837.JPG) <br>
2. Use the sox to convert the flac format to wav format as: **sox listen_up.flac listen_up.wav** <br>
3. Use the sox to convert wav to raw as: **sox listen_up.wav listen_up.raw** <br>
4. Make it executable: **chmod +x listen_up.raw** <br>
5. Execute the executable: **./listen_up.raw** <br>

![2](https://user-images.githubusercontent.com/44412255/80645681-75106880-8a39-11ea-937a-c5e1a1d05193.JPG)<br>
