---
layout: post
title:  picoCTF writeups- Practice
---


A blog consisting of writeups for the practice section on picoCTF, with the necessary underlying forethoughts and tools and/or concepts used.

---

### 1. Obedient Cat:  

```cat flag```
the flag is in the direct output  

---

### 2. Mod 26:  *Cryptography*  

pass the given text through any ROT13 decoders  

> ROT13 is a special case of Caeser Cipher, where the string is rotated by 13 positions. Since, the number of rotations are known, it is more easily break-able than even Caeser Cipher, and hence of no practical usage.  

---

### 3. Python Wrangling:  

```
wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py
python3 ende.py -d flag.txt.en
```

``` cat pw.txt ```  
and enter that in the prompt as given by the python script

> wget command is used to retrieve content from web servers
> -d taken in the python command, as per usage defined by the script  

---

### 4. Wave a Flag:  

``` 
wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm  
chmod +x warm  
./warm  
./warm -h
```  

> -h passed because of the promt as given by the executable file  

---

### 5. information:  *forensics*  

metadata of the jpg file to be seen  
followed the writeup: [this](https://ctftime.org/writeup/26973)  

found a really cool site that pretty much uses all the tools in one place for image analysis: [this](https://aperisolve.fr/96a7f666c0bf82891135e98c8c2e5bea)  

the text in the license looks off to the trained eye, passing it through a base64 decoder gives the flag  

> Base64 encoding schemes are used when there is a need to encode binary data that needs to be stored and transferred over media that are designed to deal with ASCII

---

### 6. nice netcat:   

``` nc mercury.picoctf.net 35652 ```

you get a list of number in the output  

convert the decimal values as obtained in the output to ascii. I used [this](https://onlineasciitools.com/convert-decimal-to-ascii) as the online converter  
the flag is as obtained

#### 6. a) what's a net cat?  

Use the given url and port in the format as previous question. For documentation about netcat refer to [this](https://linux.die.net/man/1/nc)  

#### 6. b) Lets Warm Up  

enter the given hexadecimal as x70 in [this](https://www.rapidtables.com/convert/number/hex-to-ascii.html) converter to convert it to the corresponding ascii value  

---

### 7. Transformation:  *reverse engineering*  

The file enc, that has been given, on running a cat command with it, we get a string of seemingly chinese characters.  
First approach was to try and translate it, but it doesn't make sense in even chinese translation, so this possibility is rejected.  
next approach was to use the file command in CLI and it gives the type of the file as UTF-8. But a simple decryption of UTF-8 doesn't work either.  

So, instead used [this site](https://gchq.github.io/CyberChef/)  
put the string as obtained on the terminal as input and run the magic command in the given site. It runs a brute force attack to figure out which decryption algorithm works the best in this context. Select the intensive mode.  

![image](https://user-images.githubusercontent.com/72693136/167391995-a6012262-efc1-4914-969a-78efefdfce68.png)

this is the result as obtained on scrolling through the given outputs.  

> UTF- 16 aka 16-bit Unicode Transformation Format is a character encoding capable of encoding all 1,112,064 valid character code points of Unicode.  
  It differs from UTF-8 in the sense that UTF-8 is used for only latin(english) characters whereas UTF-16 encompasses all, as shown in the chinese character to ascii   transformation.   
  for more details regarding UTF-16 refer to [this](https://en.wikipedia.org/wiki/UTF-16)  
  
Another approach to the abovementioned problem is given in [this writeup](https://github.com/vivian-dai/PicoCTF2021-Writeup/blob/main/Reverse%20Engineering/Transformation/Transformation.md)  


