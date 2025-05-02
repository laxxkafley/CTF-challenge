Problem 

Can you crack the password to get the flag?

Hint

There are 100 potential passwords hardcoded in the script. Only one is correct.

First, I downloaded the three files as instructed:
level4.py (password checker script)
level4.flag.txt.enc (encrypted flag)
level4.hash.bin (MD5 hash of the correct password)


I used cat level4.py to read the code. 

The function level_4_pw_check() asks for a password, hashes it using MD5, and compares it with the precomputed hash stored in level4.hash.bin.

The encrypted flag is decrypted using a custom XOR function called str_xor, which uses the correct password as the key.

3. Plan
The code includes a list of 100 possible passwords:

pos_pw_list = ["158f", "1655", "d21e", ...]

So my plan was:

Loop through this list.

For each candidate, compute the MD5 hash.

Compare it with the correct hash from level4.hash.bin.

If it matches, use it to decrypt and print the flag.


I edited the bottom of the script to automate password testing. I replaced the level_4_pw_check() call with:

for pw_str in pos_pw_list:

    if hash_pw(pw_str) == correct_pw_hash:
    
        print("Password is correct:", pw_str)
        
        decrypted_flag = str_xor(flag_enc.decode(), pw_str)
        
        print("Flag:", decrypted_flag)
        
        break
        
This brute-forces the password by testing all 100 options without manual input.


I ran the modified script:
python3 level4.py

And successfully found the correct password and decrypted the flag:

