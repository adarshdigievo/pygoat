## Lab 1 (SQL Injection)

- Mission: Log-in as admin
- Code: [views.py sql_lab() line:157](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:157
  )
- First you need to login to the Pygoat application as superuser (as mentioned in `readme.md` project setup).
- Go to the [SQL injection lab page](http://localhost:8000/injection) and inject SQL commands to gain access.
- Inject `anything' OR '1' ='1` as the password
- See the SQL query in the Django app logs.

## Lab 2 (Command injection Lab 1 in Pygoat)

- Mission: Execute arbitrary code on the server
- Code: [views.py cmd_lab() line:416](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:416
  )
- Go to the [command injection lab 1](http://localhost:8000/cmd)
- Perform injection by combining a domain + a command (`google.com & dir`)
- The command will be executed in servers shell
