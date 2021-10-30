# Magikarp Ground Mission 

This one was easy, simply SSH into an instance and `cat` out the contents of 3 files to get the flag. 

Here were my commands: 
```
    1  ls
    2  cat 1of3.flag.txt
    3  cat instructions-to-2of3.txt
    4  cd /
    5  ls
    6  cat 2of3.flag.txt
    7  cat instructions-to-3of3.txt
    8  cd ~
    9  ls
   10  cat 3of3.flag.txt
```

##
Flag: `picoCTF{xxsh_0ut_0f_\/\/4t3r_c1754242}`
