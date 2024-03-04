# Mind Ur Ps and Qs

An RSA key depends on n being unfactorizable to p and q but the n here is small enough to be factorizable, doing so we get p and q, running then throught his code i found on 
stack overflow, 

```
# Code from https://stackoverflow.com/questions/4798654/modular-multiplicative-inverse-function-in-python

def egcd(a, b):
    if a == 0:
        return (b, 0, 1)
    else:
        g, y, x = egcd(b % a, a)
        return (g, x - (b // a) * y, y)

def modinv(a, m):
    g, x, y = egcd(a, m)
    if g != 1:
        raise Exception('modular inverse does not exist')
    else:
        return x % m

p = 1617549722683965197900599011412144490161
q = 475693130177488446807040098678772442581573

n = p * q
phi = (p-1)*(q-1)
e = 65537
d = modinv(e,phi)

c = 8533139361076999596208540806559574687666062896040360148742851107661304651861689
plain = pow (c,d,n)
print(plain)
print(hex(plain))
print(bytearray.fromhex(hex(plain)[2:]).decode())
```

FLAG: picoCTF{sma11_N_n0_g0od_45369387}

![Screenshot 2024-03-05 040745](https://github.com/nAYANko/picoCTF/assets/147973815/4e2b47aa-1172-4729-9798-719e39c4fd51)

![Screenshot 2024-03-05 043423](https://github.com/nAYANko/picoCTF/assets/147973815/56a78a4a-854a-48b7-b08e-b2249e3d645c)



