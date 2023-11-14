# picoctf

# keygenme-py

We need to figure out what key_part_dynamic1_trial to get the flag. I went throught the code and found out that the check_key function takes the hexdigest of the  
sha256 hash of b"FREEMAN" and then selects a certain character by an indexing to a certain point on that string.

Then I simply used a for loop and found out the hexdigest of the sha256 hashes of b"FREEMAN",got the characters in the given indices and printed the final key.


```
import hashlib
import base64

username_trial = b"FREEMAN"

key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
key_part_dynamic1_trial = "xxxxxxxx"
key_part_static2_trial = "}"


indices = [4,5,3,6,2,7,1,8]
key_part_dynamic2_trial = ""
#hashlib.sha256(username_trial).hexdigest()[4] == key_part_dynamic1_trial[0]

for i in indices:
    key_part_dynamic2_trial += hashlib.sha256(username_trial).hexdigest()[i]

key_full_template_trial = key_part_static1_trial + key_part_dynamic2_trial + key_part_static2_trial
print(key_full_template_trial)
```
