## DOCKER LEARNING

### pull a docker image from docker hub
```docker pull <image name>```

### run a docker image
```docker run <image name>```

### pull and run in one step
- if image will not be in machine then first it will pull and after that will run

```docker run <image name>```

### run an image in interactive mode

```docker run it <image name>```

### list out the running process
- list running process

```docker ps```
- list all processes running and closed

```docker ps -a```

### basic linux 
#### apt
package manager in linux

```apt install <package name>```

list all the packages available in apt database

```apt list```

if the package is  not available in database then update the database

``` apt update```

### Linux directory structure
in linux everything is file
/
* bin -- related to binaries
* boot -- boot related files
* dev -- devices related files
* etc -- editable text configuaration  related files
* home -- home directory for user
* root -- home directory for root user only root can access
* lib -- directory for libraries
* vat -- variable
* proc -- related to running processes

```ls```
```ls -a```
```ls -1```

```cd ~``` -- navigate to user's home directory

```pwd```
```whoami```

```mv``` --used to rename/move a file or directory

```rm```  --used to remove a file or directory

#### view the content of directory in linux
```cat```

```more```  -- we can only scroll down

```less```  -- we can scroll up and down

```head```
```tail```

```grep```

```find```

### running mutliple commands
### chaining commands 

``` comand1 ; command2 ; command3```

``` comand1 && command2 && command3```

``` comand1 || command2 || command3```

### piping command

```ls /etc | less```


### adding viewing environment var

```printenv```

```printenv PATH```

```export DB_USER = local_user``` --this environment variable will persist for current shell only

for persistant changes add the variable in .bashrc file  available in root directory ls -a

```echo DB_USER=local_user>>.bashrc```

when you will add the variable in .bashrc file and try to view the variable using echo $var_name it will not show as the file is loaded at starting so need to rerfresh

```source .bashrc```

```ps```

```kill <process_id>```


```useradd  <user name>```
```usermod```
```userdel```

```adduser <username>```

### open new shell in docker

```docker exec -it -u <username> <container id> bash```


#### changing the permission of a file

```chmod u+x <file name>```

u+x
o+x
g+x
u-x
o-x
g-x
rwx --> read write execute





### image vs container

* an image contains cut down os and all the configuration files needed to run that

* a container is like virtual machine, provides an isolated environment
* a container can be stopped and restarted


## DOCKERFILE
- FROM
- WORKDIR
- COPY
- ADD
- RUN
- ENV
- EXPOSE
- USER
- CMD
- ENTRYPOINT

### build image

```docker build -t <tag name> .```

. --> used for specifying that dockerfile is in current directory


### COPY VS ADD

copy and add works simillar except add have following features
- add can add the files from url
- add can uncompress a zip file and copy that


### note
when its copying the data from directory it can only copy the dockerfile directory or subdirectory content and not from uplevel director as when docker client passes the context to docker engine it doesn't have to access other thant that

