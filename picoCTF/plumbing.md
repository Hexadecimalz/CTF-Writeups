# plumbing 
Connect using netcat and find a way to save the output to a file and find the flag. 
I first tried to redirect the output using `>`, but that didn't work. The second hint mentions piping the output. We can use the `tee` command to do just that. 

```
nc *.*.*.org 14291 | tee output.txt 
# press control+c to end when done 
cat output.txt | grep pico 
# flag = picoCTF{digital_plumb3r_ea8bfec7}
```
