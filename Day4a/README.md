# Day 4a

## Issues that I faced

- Apache could not start because port 80 was already being used.
- I had difficulties configuring DNS and understanding domain mapping.
- Certbot could not be configured successfully on UTM.
- Some MariaDB commands were unavailable in my environment.

## Additional Server Service

I chose Docker as my additional server service.

Commands used:

sudo apt install docker.io -y

sudo systemctl start docker

sudo systemctl enable docker

docker --version

sudo docker run hello-world

The installation was successful and the Hello World container ran correctly.
