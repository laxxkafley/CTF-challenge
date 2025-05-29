❓ Question: Unzip

Description:

Unzip this archive and find the flag.
File: big-zip-files.zip

✅ Solution:
📥 Step 1: Download and unzip the file
I downloaded the zip file from the challenge and unzipped it:

unzip big-zip-files.zip

This created a folder named big-zip-files/ with many subfolders and files inside.

🔍 Step 2: Search for the flag using grep
Since there were too many files to check manually, I used grep to search for the flag pattern:

grep -R "picoCTF" big-zip-files

This command searches recursively (-R) through all files in the big-zip-files folder for any line that contains the word "picoCTF".

🏁 Found this result:

big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years.

Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

🎯 Final Answer:

picoCTF{gr3p_15_m4g1c_ef8790dc}
