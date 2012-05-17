# Lightning Talks
host by Dr. Nic

## Talks

### Dan Hassin: NS Rails

* High-level APIs that give your Object-C classes
* Drop-in framework 
* http://github/dingbat/nsrails @2nf340

### Wind Tunnel

* Headless BDD javascript testing tool

### Tony Arcieri

config.threadsafe = true

railsplugins.org thread safety

	require_dependency

JSONP does threading with Worker()
	importScripts
	
### iwanttolearnruby.com

### Work distributed
As part of private team:
Work as if you were distributed
Use hipchat / campfire with your team

### Simple Background workers
Sidekiq in 1 minute
sidekiq/capistrano

### Modeling on Rails

gem 'erd' allows dynamic editing of models

### Integrating Engines Testing

Your::Engine.routes.draw
mount Your::Engine, :at => 'path'
isolate_namespace is the right way of doing
	your_engine.people_path
	main_app.people_path
	get :index, :use_route => :spree
	visit spree.products_path

## Takeaway