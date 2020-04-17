# Watergun Assassin Platform

### Environment, infrastructure and setup related files for the Watergun Assassin project

## Install the platform

Make sure you have Docker and Docker Compose installed on your computer

### Clone all repos

In order to run the application, make sure you have cloned this repo, as well as the following repos, into the _same folder_ on your computer:

-   [Watergun Assassin Frontend](https://github.com/jakepatrickw/WA-front-end)
-   [Watergun Assassin Backend](https://github.com/jakepatrickw/WA-back-end)

### Run the Docker Compose project

There are two commands you can use to run the platform, depending on how much information you want to see. Use your terminal and navigate to this project (the platform repo) and run one of the following commands. Note that either of these commands will take quite a bit of time to run the first time, because docker will need to build your images before spinning up your containers and starting the development servers inside them.

#### Running to see debug messages

> docker-compose up

This command will start up your development environment and will continue actively running in a terminal. Any debug messages (set up messages from Docker as it spins up your container, logs to the console from your javascript or python programs) will be printed into the terminal. This can be really useful if you want to get a feel for what is going on when docker spins up your project, or if you need to debug something from the frontend or backend project through console logging. In order for the development environment to continue running when you have used this command, this terminal window needs to stay open. When you close the window, docker will spin down your development environment. (This is fine, you can just spin it back up again whenever you're ready).

Use if:

-   You want to see debug or setup messages
-   Your containers are failing to start up for some reason. The failure messages will be printed to the terminal.

#### Running in the background

> docker-compose up -d

This command uses the `-d` flag to run your containers in daemon mode. This means that your containers run as background processes. The command will print out a message that each container is starting to create, and then it will exit. Your containers will continue to spin up in the background (as long as they don't encounter any fatal errors) and you can close the terminal or use it for something else.

Use if:

-   You want to run your containers in the background

#### Checking what containers are running

> docker ps

This command will list all containers that are running.

#### Viewing the local web services

Frontend: http://localhost:1234
Backend: http://localhost:8000

Once your containers are spun up, you can visit the frontend and backend sites at the above addresses. If they are not showing up, give it a minute or two, even if your containers say they are done spinning up and the servers are ready. I have noticed a bit of a delay.
