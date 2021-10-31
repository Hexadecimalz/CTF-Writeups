# Some Assembly Required 1
http://mercury.picoctf.net:1896/index.html

Page redirects to a web form asking us to submit the flag.  

## Solution 
At first glance we can see there is some simple HTML and a Javascript companion located at `G82XCw5CX3.js`. Back in the day when I was first learning HTML and Javascript it was very common to obfuscate code to prevent people from stealing it or otherwise knowing what was going on. There were sites to type in your code and compress it into a single line. At the time it was assumed that everyone was looking at your code all the time. People went so far as to prevent right-clicks, so you couldn't steal their code. 😁

My first thought was to unobfuscate the code to get a better grasp of what was going on. Cyber Chef helped a little. Try JavaScript Beautify and the result is marginally better than before. Try JavaScript Parser and maybe even a little better with a JSONified look. 

I couldn't make heads or tails of it until looking at another writeup, which mentioned tthat there was a path involved. Simple, yet elusive. 

## Flag 
`picoCTF{a2843c6ba4157dc1bc052818a6242c3f}`

## Resources 
[vivian-dai's - Writeup](https://github.com/vivian-dai/PicoCTF2021-Writeup/blob/main/Web%20Exploitation/Some%20Assembly%20Required%201/Some%20Assembly%20Required%201.md)
