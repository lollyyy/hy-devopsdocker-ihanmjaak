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

## Exercise 1.5 

Command to start the container `docker run -d -it --name curl-ubuntu ubuntu:16.04 sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'`

Entering the container with `docker exec -it d8a bash`

### Installing CURL

Installing CURL inside the container by first running `apt-get update` to update Ubuntu, then install CURL with `apt-get install curl` 

### Retrieving a website with CURL

Attach to container with `docker attach curl-ubuntu`, the container now waits for input. Entering `helsinki.fi` returns the following:

```html
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html> 
```

## Exercise 1.6

The Dockerfile for this exercise can be found [here](https://github.com/lollyyy/hy-devopsdocker-ihanmjaak/blob/master/part1/1.6/Dockerfile)

---

The commands used for this exercise:

Various different commands such as `docker run devopsdockeruh/overwrite_cmd_exercise` used in great confusion before a quick search from the course Telegram chat cleared out what do I need to do in this exercise

`docker build -t docker-clock .` to build the container from the Dockerfile

`docker run docker-clock` to run container

## Exercise 1.7

The Dockerfile for this exercise can be found [here](https://github.com/lollyyy/hy-devopsdocker-ihanmjaak/blob/master/part1/1.7/Dockerfile). And the script file [here](https://github.com/lollyyy/hy-devopsdocker-ihanmjaak/blob/master/part1/1.7/script.sh)

Used `docker build -t curler .` to build the Docker container from Dockerfile, after that `docker run -it curler` to run said container

Running the container prompts a website query and entering `helsinki.fi` returns the following:

```html
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="http://www.helsinki.fi/">here</a>.</p>
</body></html>
``` 

## Exercise 1.9

Command used for this exercise: 
`docker run -d -p 3000:80 devopsdockeruh/ports_exercise`



