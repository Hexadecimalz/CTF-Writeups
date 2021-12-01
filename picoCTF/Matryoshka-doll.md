# Matryoshka doll 🎎

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: this. 

Category: Forensics 

## Hints 

> Wait, you can hide files inside files? But how do you find them?

## Solution

We have a photo of a Russian Matryoshka doll, but not much else to go off of. At first, I considered maybe a steagnographically embedded file of some sort, but figured I was over-complicating for picoCTF style challenges. Because the hint suggested a file I thought it would not be worthwhile to check the EXIF data for the flag.  

I checked a writeup for some guidance and found they used a tool called binwalk. Not surprisingly they also have -M option for matryoshka, pretty good hint on that one. Although this option is not using, just run the command `binwalk dolls.jpg` and the additional zip file is listed. After using `unzip` about 4 times on the resulting files the flag is presented in a text file. 

## Resources 

- [PoC Innovation - writeup](https://ctftime.org/writeup/26903)


