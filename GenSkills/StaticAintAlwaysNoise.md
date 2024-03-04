# Static Ain't Always Noise

So here we have a static file which is an ELF 64bit file, looking into a file the bash file, we have a shell script that basically does object dump on a given argument, the file static in our case. 

![static1](https://github.com/nAYANko/picoCTF/assets/147973815/65f14aa2-56ac-408b-a0cc-baabc7985b1d)


We modify the bash file permissions using `chmod +x ltdis.sh` to make it an executable.
After that we run the file and pass static as argument `./ltdis.sh static`.
We get 2 file, one has the strings and other is the object dump, in the object dump we can see al the low level assembly code,
catting out the strings file gives and a bunch of strings and the flag can be found within

![static2](https://github.com/nAYANko/picoCTF/assets/147973815/abb367da-9f9a-41a5-87fc-c58c958b734d)


Flag: picoCTF{d15a5m_t34s3r_f6c48608}
**************************

ALTERNATIVELY

We can also use
```
strings static | grep picoCTF
```
but the challenge was meant to teach us how a basic object dump does and the above code is actually all it does.



