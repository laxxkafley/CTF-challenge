2. SSH Challenge (picoCTF)
For this challenge, I was tasked with accessing a remote server using SSH and retrieving a flag. The challenge provided a username (ctf-player) and a password, and the server was hosted at titan.picoctf.net on port 52265. To begin, I ran the SSH command to connect to the server:
ssh ctf-player@titan.picoctf.net -p 65335. Once I connected, I was prompted to confirm the server's fingerprint, to which I typed yes to proceed. I then entered the password provided in the challenge description when prompted. After logging in, I navigated to the directory containing the flag and used the cat command to view the file:
cat flag.txt. The flag appeared in the terminal in the format:
picoCTF{ssh_flag_retrieved}. This flag marked the successful completion of the SSH challenge.
