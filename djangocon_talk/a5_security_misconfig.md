## Lab 1 (A5 Security Misconfiguration Lab 1 in Pygoat)

- Mission: Enter the admin page where a secret visible only to 
admin can be found.
- Code: [views.py line:576](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:576)
- Go to [Lab page](http://localhost:8000/sec_mis) and open Lab 1.
- Based on the error message, a check is done on an X-HOST header
- We can intercept the request, modify it from client side to 
add the header and resend it. Now the attacker has access to the secret.
- In this case, Pygoat gives out the necessary info for attackers 
to attack. However, in real world, 
attackers will perform a number of similar attacks.
- Attackers will check if all validations or verifications happen in the 
backend rather than relying on frontend supplied values. 
They will try modifying header values, change the request parameters, ids , etc. and 
see how the application behave.

## Lab 2 (A5 Security Misconfiguration Lab 2 in Pygoat)

- Mission: See a secret env variable stored in the server.
- Code: [settings.py line:30](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=pygoat/settings.py:30)
- Go to [Lab page](http://localhost:8000/sec_mis) and open Lab 2.
- We need to expose a sensitive env variable
- Trigger a 404 page by opening an invalid url. Since it shows all 
possible routes, we can understand that Django debug
  mode is enabled.
- A real attacker would test out all the pages for any sensitive data 
exposure. When the application produces a 500
  error, the env is dumped to the UI.
- We have a readily made [500 error page](). Its code is
  at [views.py error(): 433](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:433)
