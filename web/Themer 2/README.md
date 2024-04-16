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

Analyse the code provided inside `chall`>`app`>`server.py`. We see that any occurence of "../" is changed to ""(empty string) in the theme argument.

> Lines 8 - 13

```C
    safe_theme = request.args.get("theme", "themes/theme1.css")
    if safe_theme[0] == "/":
        safe_theme = safe_theme[1:-1]
    safe_theme = safe_theme.replace("../", "")    // "?theme=../flag.txt" will be read as "?theme=flag.txt" causing error.
    f = open(safe_theme, "r")
    theme = f.read()

```

Now if we give path traversal as `?theme=.../...//flag.txt`, it will be read as `?theme=../flag.txt` as all the occurences of "../" are removed.
Reloading the page gives the flag in the source code.

## Flag

COPS{path_traversal_yay_291}
