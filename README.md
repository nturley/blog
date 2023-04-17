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

## Induced Demand

A counter-intuitive law of urban
planning is that widening roads doesn't
reduce congestion, it just increases the
number of cars. I guess the assumption
is that the maximum number of cars that
could possibly be on this road are so
high that there simply is no amount of
road sufficient to carry them all, so
the game of trying to out-build traffic
is a fools errand.

The mistake here, is assuming that all of the
variables will remain the same while
you change one of them. This is very similar
to the oft cited concern that automation will reduce
employment. The assumption is that once
a job becomes automated, the people that
had that job will become unemployed. This may very well be true in the short term, but it's hard to imagine a long term state
where people remain unemployed because there is literally nothing for them to do. What seems more likely is that the supply
and demand for different types of labor at different parts of the world will move around due to technological, cultural, and
political changes.

Because of automation, the power of what a human can do is increased. Someone using a sewing machine can make many more shirts
than someone sewing them by hand. As a result, it requires fewer seamstresses to create the same number of shirts, so a poor
assumption to make would be that employment for seamstresses would decrease, but in fact, if an employer were able to convert
their hand sewing seamstresses into machine sewing seamstresses, they would simply increase their production, reduce their prices,
gain a larger market share than their competitors, make more profit because of their reduced margins, which would allow them to
hire more seamstresses to further increase their market share until the shirt market becomes saturated at this price. If the
labor market was competitive, and they are unable to hire more seamstresses, then they may be forced to increase seamstress pay
to attract more labor (perhaps from their competitors). The employer can afford to do this because the productivity for seamstresses
has risen so much, that their value to their firm is increased. So in this simple hypothetical situation, seamstress employment
increased, the pay increased, the price of shirts decreased which are all positive outcomes for society at large.

In the above hypothetical, the firm was able to convert their existing employees from low productivity tech workers to high
productivity tech workers and theoretically machine sewing shirts isn't that much worse than hand sewing them so nearly everyone
benefited from the technology disruption that sewing machines brings to this industry. However, suppose that these types of sewing
machines are upgraded again into giant industrial machines that churn out shirts with nearly no manual intervention. The labor cost
per shirt drops to nearly nothing and nearly the entire cost of shirt is due to the cost of materials. Instead of seamstresses, the
firm now needs mechanics and automation professionals which come from a very different labor market than their existing employees.
So they have no need of seamstresses any longer so they fire them all. Meanwhile the massive increase in shirt material consumption
has driven up the prices and so the labor market in the textile industry has expanded but it is not as large as the seamstress industry was
and so the unemployed seamstresses all take jobs in the textile industry, which floods the labor market and depresses the pay.
So the price of shirts has plummetted. The seamstresses are working for less money.


