# pretix-docker_compose
A full config to run pretix with docker-compose

Than run the docker-compose file and create a new cronjob to run the internal pretix jobs.

```
15,45 * * * * /usr/bin/docker exec pretix_app pretix cron
```

For us it is enough to run `docker exec -it pretix bin/bash` and then execute `pretix cron` inside the container.

After starting the stack navigate to:
https://localhost:80/control/

The default user is: admin@localhost
And the default password is: admin

Change this settings!