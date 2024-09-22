## Lab 1

- Mission: Get acess as admin and view a secret visible only to admin users
- Pygoat A7 [Lab 1](http://localhost:8000/auth_failure)
- Code: [views.py Otp() line:489](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:489)
- The application allows for login without password using an OTP. Rate limits are not applied.
- We can attempt to login as admin@pygoat.com by using OWASP ZAP to brute force the OTP. For that we need to find the POST request sent with OTP and fuzz that.