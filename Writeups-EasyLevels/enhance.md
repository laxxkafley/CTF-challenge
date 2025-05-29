❓ Question: Enhance!

Description:
Download this image file and find the flag.
File: drawing.flag.svg

✅ Solution:
📥 Step 1: Download the file using wget

wget https://artifacts.picoctf.net/c/541/drawing.flag.svg
This downloaded the file drawing.flag.svg to my current directory.

👀 Step 2: Read the file using cat

cat drawing.flag.svg
The file is in SVG (Scalable Vector Graphics) format, which is XML-based.

Inside the file, I found <text> and <tspan> tags with very tiny font-size values.

These tags contained scattered characters that looked suspiciously like parts of a flag.

🧩 Step 3: Extract the flag from the text
From the SVG content, I saw:

xml
Copy
Edit
<tspan>p </tspan>
<tspan>i </tspan>
<tspan>c </tspan>
<tspan>o </tspan>
<tspan>C </tspan>
<tspan>T </tspan>
<tspan>F { 3 n h 4 n </tspan>
<tspan>c 3 d _ 2 4 3 7 4 6 7 5 }</tspan>
I manually combined all the characters to reveal the full flag.

🎯 Final Answer:

picoCTF{3nh4nc3d_24374675}











Tools


