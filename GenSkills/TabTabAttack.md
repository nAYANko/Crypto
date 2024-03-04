# Tab Tab Attack 

We have a zipped file, unzipping it gives a directory, leading to another directory and another and another, instead of changing 1 by 1 we can just press tab multiple times to autofill the availaible directory making our task faster.

![tabtabattack1](https://github.com/nAYANko/picoCTF/assets/147973815/1be2e594-1a62-46ba-8cfb-b7c2e16c37d7)

At the end we get an ELF file, use strings piped with grep picoCTF to get the flag.

Flag: picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
