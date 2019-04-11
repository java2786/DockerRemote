Run commands on remote Docker host

Use docker client to connect with remote docker host, without local Docker installation.
1.	Download Docker client from http://download.docker.com
2.	Unzip the download to a folder where docker.exe & dockerd.exe are extracted.
3.	To use docker command in your system from any location, add current location (path where docker and dockerd commands are saved) in environment PATH variable.
a.	Note: Do not change previous string. Put  “;” at the end if not there and paste the path where docker.exe is placed.
4.	 docker -H:172.18.2.50:2375 will connect to docker running on remote host
docker -H:172.18.2.50:2375 info
docker -H:172.18.2.50:2375 run hello-world


5.	We are done. Below steps are optional now but makes it easy to use docker
6.	Try to save docker -H:172.18.2.50:2375 as a command
7.	Navigate to the folder where docker.exe is placed and create dockerx.bat file which contains:
docker -H=172.18.2.50:2375 %*
8.	Now in your system, dockerx command will be used to connect to docker running on remote host
 dockerx info
 dockerx run hello-world
 dockerx images
9.	Here dockerx will be replaced by docker -H=172.18.2.50:2375 and you will connect to docker running at remote host.

