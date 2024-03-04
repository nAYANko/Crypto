# GET aHEAD

For this install burpsuite and run the file there so analyse network vulnerablities, after running the link in the burpsuite browser we can see that there is a POST request and GET requests, from the challenge name we can conclude that we need a GET and HEAD method, so we take the POST method add it to the repeater which basically repeats the request but with modifications, we change the method to HEAD and we get the flag.

FLAG: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}

![getahead1](https://github.com/nAYANko/picoCTF/assets/147973815/2a5b3c69-6dcf-4386-b398-0b064fea0a7d)

![getahead2](https://github.com/nAYANko/picoCTF/assets/147973815/e2bb62a7-9a4d-42a1-a8ea-cc1f28e1ccb5)

*********************************

An alternative method is using curl command,

```
curl -X HEAD http://mercury.picoctf.net:53554/index.php --head
```

This also gives the flag instantly.
