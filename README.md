# dbconnect
Development container for databricks-connect (pyspark)

# Requirements
- Docker and [WSL2](https://devblogs.microsoft.com/commandline/announcing-wsl-2/) if using windows
- VS Code with [Remote Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). Other IDEs does provide similar capabilities, but are not documented here.

# Build the docker image:
1. Build the container using "docker build -t dbconnect ."

## Getting Started

1. Open an empty or existing project folder in VS Code
2. Create a directory called .devcontainer (add it to .gitingore)
3. Create an empty file in the directory called devcontainer.json
4. Paste this code into the file (made for windows 10. Adjust for OS):

```
{
    "context": "..",
    "image": "dbconnect",

    "settings": {
        "python.pythonPath": "/opt/conda/envs/dbconnect/bin/python",
        "python.venvPath": "/opt/conda/envs/dbconnect/lib/python3.7/site-packages/pyspark/jars"
    },

    "containerEnv": {
        "DATABRICKS_ADDRESS": "${env:DATABRICKS_ADDRESS}",
        "DATABRICKS_API_TOKEN": "${env:DATABRICKS_API_TOKEN}",
        "DATABRICKS_CLUSTER_ID": "${env:DATABRICKS_CLUSTER_ID}",
        "DATABRICKS_ORG_ID": "${env:DATABRICKS_ORG_ID}",
        "DATABRICKS_PORT": "${env:DATABRICKS_PORT}"
    },
    "extensions": [
        "ms-python.python"
    ]
}
```

5. Set the environmental variables for your system. Optionally add any additional extensions you want to the extensions block.

**IMPORTANT: Changing any setting in the devcontain.json after the container has been build requires you to rebuild the container for it take effect**

To open using Docker locally:
6. Click on the Green icon in the bottom left of VSCode and select "Reopen in Container"

# Credits
- Thanks to [Krallin](https://github.com/krallin/tini/) for the Tini init for containers.
- Thanks to [DataThirstLtd](https://github.com/DataThirstLtd/databricksConnectDocker) for inspiration

# Other resources
- [docker.com](https://docs.docker.com/get-started/overview/)
- [PyCharm with docker](https://www.jetbrains.com/help/pycharm/using-docker-as-a-remote-interpreter.html)
- [VS Code remote container](https://code.visualstudio.com/docs/remote/containers)