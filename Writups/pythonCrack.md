Problem:

The challenge asks: "Can you crack the password to get the flag?"
You need to download a password checker and the encrypted flag file. Then, use the checker to decrypt the flag.

Solution:
Download the Files:
First, I downloaded everything from the challenge. This gave me three files:

pw.txt (the password)

flag.txt.en (the encrypted flag)

ende.py (the script)

Check How to Use the Script:
I tried running python ende.py, but it gave me an error. So, I tried python ende.py -h to check the usage of the script. It told me that I needed to use -d to decrypt or -e to encrypt.

The exact command to decrypt was:

Usage: ende.py (-e/-d) [file]
Examples:
  To decrypt a file named 'pole.txt', do: '$ python ende.py -d pole.txt'
Decrypt the Flag:
Once I knew I needed to use -d to decrypt, I ran the following command:

python ende.py -d flag.txt.en
The script asked me for a password, so I opened pw.txt and saw the password ac9bd0ffac9bd0ffac9bd0ffac9bd0ff. I entered this password and pressed Enter.

And then I got the flag
