# Static ain't always noise 

This challenge comes with a file named `static` and a Bash script that spits out the flag in no time flat.

I put the files in the same directory and made the script executable and ran `bash ltdis.sh static`. From there the flag is easily visible. 

The script is using two programs to produce its output `objdump` and `strings`. 

If we look deeper at what is going on we can see it's an object file (looks like a library file?), which explains the static when we open the file: 

```
$ file static
static: ELF 64-bit LSB shared object, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=bedc412be2156b04706c1f2568fcff42306dea27, not stripped
```

## Resources 
- [Executables vs Shared Objects](https://askubuntu.com/questions/690631/executables-vs-shared-objects)

