Question

What is 0x3D (base 16) in decimal (base 10)?

Hint

Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.

Solution

To solve this, I first removed the 0x since it just tells me it's a hexadecimal number. That leaves me with 3D. Then I converted each digit:

D is 13 in decimal and in the 16⁰ place → 13 × 1 = 13

3 is in the 16¹ place → 3 × 16 = 48

I added them up: 48 + 13 = 61.

So, 0x3D in decimal is 61, and that was the correct flag.
