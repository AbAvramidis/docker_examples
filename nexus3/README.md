Build the image:

docker build -t nexus-abrams/ab:nex .

Run the image:

docker run -d -P nexus-abrams/ab:nex

then type "docker ps -a" see the port fordwarding 

http://host-ip:port
