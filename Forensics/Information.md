# Information

We are given a file, the first hint asks us to check file details, so we need to check EXIF data of the image to we use the `exiftool` command, here we see the licence which seems to base64 encoded, we pull the encrypted text using the following commands.

```
exiftool cat.jpg | grep License | cut -d ':' -f2 | cut -d ' ' -f2 | base64 -d
```

The second cut is important to remove the space as space is invalid in base64 so it will show an error.

![Screenshot (168)](https://github.com/nAYANko/picoCTF/assets/147973815/49c18416-5287-4275-aaae-fd1ebc6c7778)

![picoctf-Information](https://github.com/nAYANko/picoCTF/assets/147973815/4a2c9e96-6c7b-4ef4-9ef4-b9986d03d45a)

Flag : "picoCTF{the_m3tadata_1s_modified}" 
