# HoneYLoG
Shitty honeypot repo; Made by me ([@LulzAmp](https://github.com/LulzAmp)) and originally found on LulzSec's website; 
**Warning:** actually, really shitty. I tried to start it off as a small logger, it got out of hands. Might add E-Mail Support soon (if I get bored again).


1. [Configure .htaccess](https://github.com/LulzAmp/HoneYLoG/blob/master/.htaccess#L2) (.htacces: line 2; set the path to the full path to your .htpassword)
2. [Configure CloudFlare](https://github.com/LulzAmp/HoneYLoG/blob/master/index.php#L2) (index.php: line 2)
3. [Configure Users](https://github.com/LulzAmp/HoneYLoG/blob/master/index.php#L13) (honeylog.php: line 13; use [PASSWORD_BCRYPT](https://bcrypt-generator.com) to hash your passwords.)
4. You're done; have fun.

Optional: 5. remove [the following lines of code](https://github.com/LulzAmp/HoneYLoG/blob/master/.htaccess#L1-L6) from .htaccess and remove .htpasswd completely, so dumbasses won't give up on the login.
```apacheconf
# setup htpasswd
AuthUserFile /full/path/to/.htpasswd
AuthType Basic
# put whatever bullshit you want here instead of "Restricted Area"
AuthName "Restricted Area"
Require valid-user
```

> .htpassword contains **root:toor**, **admin:admin**, **Admin:admin**, **'or 1=1 /\*:'or 1=1 /*** & **'OR 1=1 /\*:'OR 1=1 /*** by default.
