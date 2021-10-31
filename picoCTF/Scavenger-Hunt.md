# Scavenger Hunt 
There is some interesting information hidden around this site http://mercury.picoctf.net:27278/. Can you find it?

## Hint 
You should have enough hints to find the files, don't run a brute force. 

## Solution 
Located in `index.html` 
```
<!-- Here's the first part of the flag: picoCTF{t -->
```

Located in `mycss.css` is also another part of the flag
```
CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0
```

Located in `myjs.js` there is a small hint, "How can I keep Google from indexing my website?" so that was a clear hint to look for `robots.txt` 
```
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```

Located in `.htaccess` 
```
# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```

Located in `.DS_Store` (file for how desktop looks on a mac) 
```
Congrats! You completed the scavenger hunt. Part 5: _a69684fd}
```
