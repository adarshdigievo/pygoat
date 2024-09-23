## Lab 1

- Mission: Run arbitrary code on the server (RCE).
- Code: [views.py a9_lab() line:602](jetbrains://pycharm/navigate/reference?project=Djangocon%20-%20Pygoat&path=introduction/views.py:602)
- Our requirements file specifies an outdated and vulnerable version of Pyyaml library.
- Open the [Lab Page](http://localhost:8000/a9), Lab 1, which is a yaml to json converter
- The file `./yaml/safe.yaml` is a simple yaml file, and it gets 
converted successfully when uploaded to the lab. 
- The file `./yaml/evil.yaml` exploits a vulnerability in the pyyaml 
library. It is crafted to run python code supplied from the frontend.
- Such a malicious file can be used to run arbitrary code on the server
- We should be careful of the application dependencies also along with our own code.