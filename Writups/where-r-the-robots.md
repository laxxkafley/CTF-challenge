blem:
Description
Can you find the robots? https://jupiter.challenges.picoctf.org/problem/60915/ or http://jupiter.challenges.picoctf.org:60915

Hint:
What part of the website could tell you where the creator doesn't want you to look?

Solution:
When I opened the link, the page asked, "Where are the robots?" I wasn’t sure what that meant at first, so I started looking at the website's code by inspecting elements, but that didn’t lead anywhere.

Then I remembered that websites sometimes have a robots.txt file, which tells search engines which pages they shouldn’t look at. I thought this might be the answer, so I tried adding /robots.txt at the end of the website's URL.

I typed this into the browser:

http://jupiter.challenges.picoctf.org:60915/robots.txt
The file showed this:

User-agent: *
Disallow: /8028f.html

That meant the robots (search engines) were told not to look at /8028f.html. So, I tried visiting that URL directly:

http://jupiter.challenges.picoctf.org:60915/8028f.html
And there it was — the flag!

