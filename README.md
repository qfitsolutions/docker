# docker


https://docs.docker.com/compose/gettingstarted/

#cd composetest
# docker-compose up

URL :  http://0.0.0.0:5000





to create seperate network:

create you own docker network (mynet123)

docker network create --subnet=172.18.0.0/16 mynet123

than simply run the image (I'll take ubuntu as example)

docker run --net mynet123 --ip 172.18.0.22 -it ubuntu bash

then in ubuntu shell

ip addr

Additionally you could use

    --hostname to specify a hostname
    --add-host to add more entries to /etc/hosts
