You can simply setup syslog-ng with docker.

```
git clone git@github.com:abdollahpour/syslog-ng-docker.git
docker build -t wpic/syslog-ng-docker syslog-ng-docker
docker run -d --name syslog-ng-docker -p 514:514/udp wpic/syslog-ng-docker
```

then you can see all the logs:

```
docker logs syslog-ng-docker
```

or you can attach to it to see live records:

```
docker attach syslog-ng-docker
```

If you press Ctrl+C you will stop the server totally. if you don't want do that:

```
docker attach --sig-proxy=false syslog-ng-docker
```

You can see some example to use syslog-ng with java [here](https://github.com/abdollahpour/syslog-ng-docker)