# flag_shop 
There's a flag shop selling stuff, can you buy a flag? Source. Connect with `nc *.*.*.org 44566` 

## Hints 
Two's complement can do some weird things when number get really big! 

## Solution 
Based on the hint I originally thought this would be something like buffer overflow, but with limited knowledge I was stuck and needed to use a local search engine for help. In the code we can see that there is an option to buy the `1337` flag, but only after you have a balance big enough to buy it. 

VermillionBird to the rescue with an explanation that mostly made sense. What I understood was that if we can make the account value negative enough the program will interpret it as a positive number in the oppositve direction, which allows us to easily buy our flag. 

In the interest of understanding more I went to Youtube for another explanation, which made a lot more sense. Two's Complement is a way that a computer can store a negative number in binary with positive numbers, since the computer can't just add a negative symbol it needs a hack to do this. 

How to get the two's complement of a number: 
1. get binary number 
2. switch 1s and 0s 
3. add 1 to the last bit 

Example(from Zanidd): 
-3 => 3 ==> 0011 ==> 1100 ==> 1101 

Moral of the story is to not pass signed integers to unsigned integers.

## Flag 
`picoCTF{m0n3y_bag5_68d16363}`

## Resources 
[VermillionBird's Writeup](https://github.com/VermillionBird/CTF-Writeups/blob/master/2019/picoCTF/General%20Skills/flag_shop/README.md)
[Zanidd's video - Integer Overflows And How They Work](https://www.youtube.com/watch?v=FE1nNDkkSRM)
[Wikipedia - Two's Complement](https://en.wikipedia.org/wiki/Two's_complement)
