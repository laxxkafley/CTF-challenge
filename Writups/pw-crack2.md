Problem:
Can you crack the password to get the flag?
You’ll need to download the password checker script and the encrypted flag file.

Solution:
Downloaded the files
I used wget to download two files:

level2.py

level2.flag.txt.enc

Then I Read the Python script
I opened level2.py and looked at the code. I found this part inside the function:

def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39) ):
        print("Welcome back... your flag, user:")
        
Figured out the password

The password is being built using chr() with hexadecimal numbers. I ran this line in Python to decode it:
print(chr(0x34) + chr(0x65) + chr(0x63) + chr(0x39))
The result was:
4ec9

I ran the script and entered the decoded password:

$ python level2.py
Please enter correct password for flag: 4ec9
Got the flag!
The script printed the flag right after entering the correct password.

