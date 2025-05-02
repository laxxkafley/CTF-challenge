Problem

"Can you crack the password to get the flag?"

Solution

So I started by downloading three files using wget:

level3.py – the main script

level3.flag.txt.enc – the encrypted flag

level3.hash.bin – the correct password’s MD5 hash

I opened level3.py and saw that it asks the user to input a password, hashes it using MD5, and compares it to the hash in level3.hash.bin. If it matches, it decrypts the flag using a str_xor function.

At the bottom of the code, there was a list of possible passwords:
["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]
At first, I just tried them one by one and got the flag, but then I thought it would be better to automate the process. So I edited the .py a little bit:

import hashlib

def str_xor(secret, key):

    new_key = key
    
    i = 0
    
    while len(new_key) < len(secret):
    
        new_key = new_key + key[i]
        
        i = (i + 1) % len(key)
        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c, new_key_c) in zip(secret, new_key)])

flag_enc = open('level3.flag.txt.enc', 'rb').read()
correct_pw_hash = open('level3.hash.bin', 'rb').read()

def hash_pw(pw_str):

    pw_bytes = bytearray()
    
    pw_bytes.extend(pw_str.encode())
    
    m = hashlib.md5()
    
    m.update(pw_bytes)
    
    return m.digest()

# List of possible passwords
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]

# Try each password
for pw in pos_pw_list:

    if hash_pw(pw) == correct_pw_hash:
    
        print(f"Correct password found: {pw}")
        
        decrypted_flag = str_xor(flag_enc.decode(), pw)
        
        print("Flag:", decrypted_flag)
        
        break
When I ran it, it printed the correct password and then showed me the flag. Problem solved!
