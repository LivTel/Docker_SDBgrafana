# Docker_SDBgrafana
Use the official grafana image to access the SDB influxdb.

About as simple as a docker setup can be. The official image is used as is without modification. 

We store our grafana configs on the big RAID and mount them into the docker container when it is started. There
are no important persistent data inside the container, so a new one can be downloaded and launched at will.

# Instructions

``git clone https://github.com/LivTel/Docker_SDBgrafana``

``cd Docker_SDBgrafana``

``docker compose up -d``

This was developed on ltvmhost5. If you start it on some other host, there may be further config required.
For example
* adding the eng user to the docker group for permissions to run docker
* reverse proxy in the front-enf web server
* mount the external RAID for the binds in the compose.yml

More information about how ltvmhost5 was configured to run docker on wiki GrafanaSDB.


