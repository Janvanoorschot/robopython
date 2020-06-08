# Running/Developing The Full Robomind Academy

## Repositories

You will need the following repositories:

* [robomindacademy](https://github.com/Janvanoorschot/robomindacademy)
* [robocontent](https://github.com/Janvanoorschot/robocontent)
* [robotjes](https://github.com/Janvanoorschot/robotjes)
* [robopython](https://github.com/Janvanoorschot/robopython)

## Build the Content
First build the executable content (gradle, jars and containers):
```bash
/data/dev/robomindacademy/bin/buildrm.sh
```

Build the content (from robocontent and robopython):
```bash
/data/dev/robocontent/robobin/bin/buildcontent
```

## Run the development environment

First from a shell run the basic support containers
(dbase, rabbitmq, robomind-runtime):

```bash
/data/dev/robomindacademy/docker/start.sh
```

Next, startup your favourite dev environment (Intellij) and start the
different repo's:

* the RMG grails-app from *robomindacademy*

This will provide an environment in which you can run traditional 
Robomind programs, interpreted by the robomind-runtime.

*  the simulation_runner from *robotjes*

This will allow you to run Python programs that are send to 'simulation_runner'
via the rabbit-mq infrastructure.


