Question:
How can you download and view the flag that is in plain sight?

Hints:
Hint 1: Any command entered into the Terminal will start with a $, and everything after the dollar sign is what you need to type.

Hint 2: To get the file accessible in your shell, you can use the wget command to download the file.

Command to use:
$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag

Hint 3: You can use the cat command to view the contents of the file.

You can check the cat manual by running man cat to learn more about how it works.

Solution:
To solve this challenge, I first used the wget command to download the file that contains the flag. The command was:
$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag

After downloading the file, I used the cat command to open and view its contents. The output displayed the flag in plain text, which was:
picoCTF{flag_in_the_clear}.

This challenge was straightforward, and I was able to retrieve the flag by simply downloading the file and displaying its contents using basic commands in the terminal.

