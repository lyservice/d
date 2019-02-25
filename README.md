# tech docs

the lyservice utility (lyserviced)

uses `<git-url>/<username>/<service>` for services (defaults to github.com/lyservice/)

services can also be added manually and can use system files rather than just git projects (you could convert systemd, runit or openrc services)

### your git repo should contain:
```
  - .ly/
  --- service.sh
```

### service.sh (used in inheritance with lyserviced):

```
# install instructions

# upgrade instructions

# update instructions

# start instructions

# stop instructions

# restart instructions

# on instruction

# off instruction

```
  
## lyservice service manager

## example
```
lyservice                     [<git-url>/][<username>/]<service>

                install

                upgrade

                update

                start

                stop

                restart

                on

                off
```

## Installing and deploying a service:
```
lyservice install service
lyservice service on (starts service and enables autostart)
```
## Updating (minor updates, no service restart)
```
lyservice update accelerid
```
## Upgrading (major updates, requiring restart of service)
```
lyservice upgrade accelerid
```
