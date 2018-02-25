# webhack

Implementing CSRF as an exercise for codepath websecurity week 4, more details:
https://guides.codepath.com/websecurity/Cross-Site-Request-Forgery

Assignments

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

ex 6. create a page with a hidden form like they show on the guide, use the url and wait for someone to load the page, see ./fake_form.html
