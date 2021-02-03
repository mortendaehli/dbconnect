# dbconnect
Development container for databricks-connect (pyspark)

# Requirements
- Docker and [WSL2](https://devblogs.microsoft.com/commandline/announcing-wsl-2/) if using windows
- VS Code with [Remote Containers Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). Other IDEs does provide similar capabilities, but are not documented here.

# Get started (Windows 10 using Docker running on WSL2)
1. set the environmental variables shown in the sample file (or handle environment variables however you want)
2. Build the container using "docker build -t dbconnect ."
3. ... work in progress... stay tuned

# Credits
- Thanks to [Krallin](https://github.com/krallin/tini/) for the Tini init for containers.
- Thanks to [DataThirstLtd](https://github.com/DataThirstLtd/databricksConnectDocker) for inspiration
- Thanks to [ContinuumIO](https://github.com/ContinuumIO/docker-images) for a starter template for Miniconda in docker


# Similar projects
- [dbconnect-docker](https://github.com/neil90/dbconnect-docker)
- [databricksConnectDocker](https://github.com/DataThirstLtd/databricksConnectDocker)

# Other resources
- [docker.com](https://docs.docker.com/get-started/overview/)
- [PyCharm with docker](https://www.jetbrains.com/help/pycharm/using-docker-as-a-remote-interpreter.html)
- [VS Code remote container](https://code.visualstudio.com/docs/remote/containers)