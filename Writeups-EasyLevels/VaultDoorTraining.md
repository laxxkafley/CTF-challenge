Description:

Your mission is to enter Dr. Evil's laboratory and retrieve the blueprints for his Doomsday Project. The laboratory is protected by a series of locked vault doors. Each door is controlled by a computer and requires a password to open.
Unfortunately, our undercover agents have not been able to obtain the secret passwords for the vault doors, but one of our junior agents obtained the source code for each vault's computer!
You will need to read the source code for each level to figure out what the password is for that vault door.
As a warmup, we have created a replica vault in our training facility. The source code for the training vault is here: VaultDoorTraining.java

✅ Solution:
📥 Step 1: Download and read the source code
I downloaded the file and used cat to read it:

cat VaultDoorTraining.java

While reading through the source code, I found the password written in a comment by the developer:

// The password is below...

// return password.equals("w4rm1ng_Up_w1tH_jAv4_be8d9806f18");

So I just wrapped that in picoCTF{...} and got the flag.

🏁 Final Answer:

picoCTF{w4rm1ng_Up_w1tH_jAv4_be8d9806f18}
