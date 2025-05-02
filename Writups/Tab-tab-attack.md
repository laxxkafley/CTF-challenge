Problem: 

Using tab-complete in the Terminal will add years to your life, especially when dealing with long, rambling directory structures and filenames: Addadshashanammu.zip

Hint:
After unzipping, this problem can be solved with 11 button-presses... (mostly Tab)

Solution:

First, I downloaded the zip file using wget with the link provided by the challenge.
Then I unzipped it using the unzip command. 
After unzipping, I used cd and Tab to auto-complete through the nested directories.
I kept pressing Tab and moving into folders until there were no more directories left.

Once I reached the innermost folder, I ran ls and found a file named something like fang-of-haynekhtnamet.
I used the following command to run the file:

./fang-of-haynekhtnamet

The flag was printed right in the terminal.
