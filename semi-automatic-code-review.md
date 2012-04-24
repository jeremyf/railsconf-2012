# Semi Automatic Code Review  
by Richard Huang

## Presentation

https://github.com/railsbp/railsbp_demo

	gem install rails_best_practices
	
	Develop -> Review
	Review -> QA
	QA -> Merge
	Merge -> Deploy
	Deploy -> Develop

Manual work…easy to introduce bugs
Automation…simple, accurate, less buggy

### "Typical Process"

#### Develop

Manually Coding
Automatic Unit Test

#### Review

Totally manual --> Could we automate?

#### QA

Automate script test
Manually verify

#### Merge

Automatic by Git
Manually fix conflicts

#### Deploy

Automatic by Capistrano

### Could we do better

Easy and maintaintable

* Following code guidelines
* Better coding syntax
* Remove unused methods

Important but complicated

* Performant
* Scalable

### rails_best_practices
analyze source code
give developers suggestions to refactor

http://github.com/logankoester/guard-rails_best_practices
rails-bestpractices-in-jenkins

https://github.com/railsbp/rails_best_practices/wiki/How-to-write-your-own-check-list

### Code Review Service?

railsbp.com

* automatically review
* collaborate with co-workers
* track history
* configure what to review

* ripper gem

## Takeaway

ripper gem
excellent software available for semi-automated code review…perfect for a lone developers

flog, flay, cane the ruby code.