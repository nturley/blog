# Neil Turley Blog

## Databases

Frequently, the assertion is made that sqlite is
sufficiently powerful to handle most use cases
where postgres is used. However frequently
the performance of sqlite is not the issue, its
how to use it. Having the database on the same
instance as the webserver means that a lot of
problems become more complicated.

For example when the database is on a separate
instance as a stateless web server, you can spin
up a second instance in parallel and start routing
traffic to the second instance and provide a
zero downtime deployment. The deployment can
include OS updates or machine configuration
changes. That becomes more complicated if your
database is on the same instance.

One way to do deployments would be to spin up a
second web server on the same instance and swap
the local network routing. The easiest way to
manage the network routing is maybe using docker
containers. The people that object to running
postgres may also be the same people that object
to docker containers but that would allow
you to swap out the machine environment your
app needs without bringing down your machine
for maintenance.

Alternatively if you run sqlite from network
storage then effectively youve separated your
state from the instance but Im not sure sqlite
was designed for that performance profile.





