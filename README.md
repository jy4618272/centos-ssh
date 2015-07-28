Official centos with openssh

with root password

# Usage
## Create Container
```
docker run -d -P --name test_centos_ssh whylu/centos6.6-ssh
```
-P for auto expose ports (22 is used for ssh)

-d for Run container in background and print container ID

--name for assign container name


You can specify root password by using -e ROOT_PW=${password}, like 
```
docker run -d -P -e ROOT_PW=password --name test_centos_ssh whylu/centos6.6-ssh
```


## Find root password and port
```
docker logs test_centos_ssh
```
```
docker port test_centos_ssh
```


## Ssh into container
ssh -p ${port} root@140.92.53.111





