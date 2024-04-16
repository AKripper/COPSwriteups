# Themer 2

Total Solves - 16

Final Score - 338

## Description 

Someone told me the previous website was broken :(((

Anyways I made it again :)

http://ctf.copsiitbhu.co.in:21339/

Author - kn1gh7

## Attachment

chall.zip

## Writeup

Upon opening the link click on any one of the themes. We can perform path traversal in the theme arguement by changing `?theme=themes/theme1.css` to `?theme=../flag.txt`.
Now we can find the flag in the source code of the page.

## Flag

COPS{path_traversal_yay_1092}
