Problem Statement:
The challenge gave me an encrypted flag that was encoded using ROT13. The flag looked like this:
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_jdJBFOXJ}. My job was to figure out how to decode it.

Solution:
ROT13 is a simple cipher where each letter is replaced by the letter 13 spots ahead of it in the alphabet. I didn't need to do it manually, so I just used an online ROT13 decoder. I pasted the encrypted flag into the decoder, and it gave me the flag:
picoCTF{next_time_I'll_try_2_rounds_of_rot13_wqKSBKJW}.

I could’ve also written a quick script to do the decoding, but using an online tool was faster and easier for this challenge. It was a good way to practice using basic cryptography like substitution ciphers.
