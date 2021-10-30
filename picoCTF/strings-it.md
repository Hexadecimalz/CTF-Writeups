# string it 

Problem: Can you find the flag in the file without running it? 

If we run the `file` command on the file we see that it's a library file: 
```
strings: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=94ec6b5e9cef175e834e0f7fcaedeaa167603c90, not stripped
```

From a previous challenge 'static' we had a bash script called `ltdis.sh`, which was able to pull flag out of the file in no time flag. No such luck this time, but it did pull out the same hint for the challenge: 
`798 Maybe try the 'strings' function? Take a look at the man page`

We can use the `strings` program to show some output `string strings`, but there is a problem the output is very large and it's making it hard to find the flag. Let's try `strings strings | grep -i pico`, which filters the extra parts we don't need and just leavesthe line with the flag. 

## Flag 

`picoCTF{5tRIng5_1T_d66c7bb7}`

