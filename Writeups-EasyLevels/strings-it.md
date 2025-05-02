Problem: Can you find the flag in the file without running it?

Solution

To solve this challenge, I first downloaded the file using wget. The file was saved as strings.1.

Then, I used the strings command to search for any readable text in the file and piped the output to grep to filter for the flag.

I ran the following command:

strings strings.1 | grep -i picoCTF

This returned the flag, and I successfully retrieved it without running the file!
