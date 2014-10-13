##Get Event Store##

A repository for http://geteventstore.com/

Shoutout to adbrowne/eventstore where I stole most of my ideas from

to expose expose http 2113 and tcp 1113 outside the container:

`docker run -d -p 2113:2113 -p 1113:1113 jmkelly/eventstore

You can access the web ui via http://172.17.8.101:2113/web/index.html

*replace 172.17.8.101 with you docker host ip address
