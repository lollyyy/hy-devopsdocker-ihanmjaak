# Part 1

## Exercise 1.1

Output for `docker ps -a` after starting 3 containers, then stopping two of them:

 CONTAINER ID | IMAGE | COMMAND | CREATED | STATUS | PORTS | NAMES
------------- | ----- | ------- | ------- | ------ | ----- | -----
97e9f5fcff68 | nginx | "nginx -g 'daemon of…" | About a minute ago | Exited (0) 13 seconds ago | | vigilant_franklin
319e1c5955c2 | nginx | "nginx -g 'daemon of…" | About a minute ago | Exited (0) 4 seconds ago | | naughty_vaughan
43a778f45a36 | nginx | "nginx -g 'daemon of…" | About a minute ago | Up About a minute | 80/tcp | romantic_banach


## Exercise 1.2

Clearing docker daemon from all images and containers

`docker ps -a:`

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

`docker images:`

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

## Exercise 1.3

Using `docker run -it devopsdockeruh/pull_exercise` we're greeted with `Give me the password:`

Navigating through Docker Hub revealed the password to be "basics" and the secret message is "This is the secret message"

## Exercise 1.4 

Run container with `docker run -d devopsdockeruh/exec_bash_exercise`

Go inside the container with `docker exec -it 697 bash`

Follow the logs using `tail -f ./logs.txt`, logs reveal us the secret message: "Docker is easy"

