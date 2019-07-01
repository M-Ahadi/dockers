In order to use this to make your Bale Bot into docker, put these files into your code directory and name your main python file to main.py

It is possible that based on the packages your bot uses, you may need to add more packages to Docker file to be installed.

Run these commands to create your docker.

```
Docker built -t your_bot_docker_name:1.0 .
docker-compose up
```