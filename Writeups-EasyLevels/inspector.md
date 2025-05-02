Problem: Inspect Me

Kishor Balan tipped us off that the following code may need inspection:
https://jupiter.challenges.picoctf.org/problem/9670/
(debug info: [u:650220 e: p: c:18 i:305])

Hints

How do you inspect web code on a browser?
There are 3 parts.

✅ Solution
To solve this, I opened the link in my browser and then right-clicked the page and chose Inspect. I checked the Elements tab and found part of the flag in an HTML comment — that was the 1/3 part.

Then, I went to the Sources tab, where all the linked files like .css and .js were listed. I looked through each file one by one. In total, I found:

1/3 of the flag in the HTML file

2/3 in the CSS file

3/3 in the JavaScript file

I combined all three parts and submitted the full flag successfully. It was a fun one!
