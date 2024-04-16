# Headers!

Total Solves - 21

Final Score - 212

## Description

Do you remember we talked about headers?

Well, use them!

Challenge Link: http://ctf.copsiitbhu.co.in:11337/

Author - kn1gh7

## Writeup

When we visit the page it says "Not an agent of the Secure-Browser"...so we go to `Devtools`>`More tools`>`Network conditions` and change `User agent` to `Secure-Browser`(Custom...).
Upon reloading the webpage it says "Does not Accept nothing" so we can use an extension like [ModHeader](https://chromewebstore.google.com/detail/modheader-modify-http-hea/idgpnmonknjnojddfkpgkljpfnnfcklj?pli=1)
to change the Request Header `Accept` to `nothing`. Upon reloading it says "Connection not secure" so we change `Connection` to `secure`. Upon reloading it says "Want-Flag is not yes"...but there is no such header as Want-Flag, 
so we create a Request Header named `Want-Flag` and put its value as `yes`. Reloading the webpage displays the flag.

## Flag

COPS{headers_all_the_way}
