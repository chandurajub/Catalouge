# CATALOGUE Service

This service is a `NodeJS` service, So we need **NodeJS** to be installed .

1. Install NodeJS

```
# curl -s https://raw.githubusercontent.com/linuxautomations/labautomation/master/tools/nodejs/install.sh | bash 
```

2. As per standards of any realtime application we do not run any service as root user. Hence we need to create one user for this application and we need to start this service with a normal user which we created.

```
# useradd catalogue 
```

3. Install the dependencies of catalogue application.

**Use Git Clone to Get Code**

Run the next commands with following settings.

User - `catalogue`

Directory - `/home/catalogue/catalogue`

```
$ npm install 
```

4. Need to import `catalogue` service to the system, To manage with `systemctl`.

```
# mkdir -p /var/log/robo-shop/
# cp /home/catalogue/catalogue/catalogue.service /etc/systemd/system/catalogue.service
# systemctl daemon-reload
# systemctl enable catalogue
# systemctl start catalogue
```