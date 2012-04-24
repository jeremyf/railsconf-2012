# Stack Smashing
by David Czarnecki
http://speakerdeck.com/u/czarneckid/p/railsconf-2012-stack-smashing-ruby-red

## Presentation

quickly need a lot of VMs…more servers, more problems

chef recipes for managing your server…mostly stock
application migration – were running on VMs and migrating to physical servers
application upgrading - 
### Unicorn 

* fast
* kernel load-balancing
* rolling restarts
* signal for capacity

### Service Configuration

Create aliases for database server names
Resque is their choice queue

### Capistrano

They gemified their capistrano apps;
Gemfile had (group :deploy)

### Application Monitoring

it must be visual
using Munin  

### Infrastructure Monitoring

BDD done on infrastructre via cucumber
rackspace-validations runs every 5 minutes

### Continuous Integration

Jenkins is used
Gem In A Box
:git => 'into your organization' shields you from infosuicide

### Continuous Deployment

Github flow…everything in master is deployable

## Takeaway
http://speakerdeck.com/u/czarneckid
http://github.com/czarneckid
http://github.com/agoragames

Cucumber to test server configuration