# Are you Admin?

Total Solves - 20

Final Score - 241

## Description

Can you get admin access?

http://ctf.copsiitbhu.co.in:21340/

## Writeup

Visiting the link it says "Are you Admin?" and rest of the text does not provide much information. If we try looking at the cookies we find a cookie named 'user' with the value 'guest'.
We can use [ModHeader](https://chromewebstore.google.com/detail/modheader-modify-http-hea/idgpnmonknjnojddfkpgkljpfnnfcklj?pli=1). to add a new cookie named 'user', this time with the value as 'admin'.
Reloading the page displays the flag.

## Flag

COPS{broken_auth_using_cookies_231}
