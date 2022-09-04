### (Play the CTF here)[https://play.picoctf.org/practice/challenge/287?category=3&page=1&search=.py]
```python
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################


flag_enc = open('flag.txt.enc', 'rb').read()
print(f"Encrypted flag: {flag_enc}")


def level_1_pw_check():
    # You can either change user_pw == to user_pw != or just copy the descyption and print it by placing it into another scope.
    # In this case I will just make it to user_pw !=
    
    print("Just press enter, This script was cracked already!\nComment out this line if you get the flag another way to avoid confusion..")
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw != "ak98" + \
                   "-=90" + \
                   "adfjhgj321" + \
                   "sleuth9000"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), "utilitarian")
        print(f"Descrypted flag: {decryption}")
        return
    print("That password is incorrect")



level_1_pw_check()
```
