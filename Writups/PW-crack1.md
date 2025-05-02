Problem:
The challenge asks: "Can you crack the password to get the flag?"
You need to download a password checker and the encrypted flag file. Afterward, use the password checker to retrieve the flag.
Solution:

Download the Files:

I first used wget to download the password checker, which saved as level1.py, and the encrypted flag file level1.flag.txt.enc.

Check the Code:

I opened the level1.py script and looked through the code. I found that the correct password was hardcoded in the script, specifically:


if user_pw == "8713":

    print("Welcome back... your flag, user:")
    
This means the password required to access the flag was 8713.

Run the Script:

I then ran the script using:

python level1.py

When prompted, I entered the password 8713.


After entering the correct password, the script printed the flag


