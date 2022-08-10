# Running Python PIP using Corporate Proxy

1. Proxy without Credential:
```shell
pip3 install --proxy=http://<host>:<port> --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org <library-name>
```

2. Proxy with Credential:
```shell
pip3 install --proxy=http://<username>:<password>@<host>:<port> --trusted-host pypi.org --trusted-host pypi.python.org --trusted-host files.pythonhosted.org <library-name>
```

> Notes: You can add more `--trusted-host` in this script 
