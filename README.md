# Random-Password-Generator
```
import random
caps = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
small = "abcdeghijklmnopqrstuvwxyz"
digit = "0123456789"
spcl = "!@#$%&^"
upper=int(input('no. of uppwecase letters\n'))
lower=int(input('no. of lowercase letters\n'))
num=int(input('no. of numerics\n'))
sym=int(input('no. of special character\n'))
def password_generator():
    password = ""
    if((upper+lower+num+sym) <  8):
        print("\nPassword should comprise minimum 8 character with at least one uppercase letter,lowercase letter,digit and special character.")
    else:
        for i in range(upper):
            password += random.choice(caps)
        for i in range(lower):    
             password += random.choice(small)
        for i in range(num):      
            password += random.choice(digit)
        for i in range(sym):
            password += random.choice(spcl)
        password = list(password)    
        random.shuffle(password)
    print(password)        
password_generator()
