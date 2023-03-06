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

