Problem :

Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too. Here's a dictionary with all possible passwords based on the password conventions we've seen so far.
We are given three files:

Solution

Step 1: I opened the file using:
cat level5.py

I saw that the script:

Takes a password input and checks it using MD5 hash

🧠 Step 2: we are given passwords in dictionary.txt file. so I need to loop through these passwords and hash them and check it with the level5.hash.bin where there is a pre computed hash.
Then I edited the code to do that.

🧪 Step 3: The Script I Used

import hashlib

# XOR function (already given in original script)

def str_xor(secret, key):

    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c, new_key_c) in zip(secret, new_key)])

# Load encrypted flag and correct password hash

flag_enc = open('level5.flag.txt.enc', 'rb').read()

correct_pw_hash = open('level5.hash.bin', 'rb').read()

# Open dictionary as text (not binary!)
with open('dictionary.txt', 'r') as f:

    passwords = f.read().splitlines()

# Hashing function (already provided)
def hash_pw(pw_str):

    pw_bytes = bytearray()
    pw_bytes.extend(pw_str.encode())
    m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()

# Brute-force loop: try all passwords
for pw_str in passwords:

    if hash_pw(pw_str) == correct_pw_hash:
        print("✅ Correct password found:", pw_str)
        decrypted_flag = str_xor(flag_enc.decode(), pw_str)
        print("🎉 Flag:", decrypted_flag)
        break
✅ Final Result
When I ran the script using:

python level5.py
I got the correct password and the decrypted flag printed on the screen.

💡 Notes:
I used 'r' instead of 'rb' to read the dictionary as plain text.

The XOR function decrypts the flag after we find the correct password.









