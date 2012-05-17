# -Ten- 42 Things You Didn't Know Rails Could Do
by James Edward Gray II

https://speakerdeck.com/u/jeg2/p/10-things-you-didnt-know-rails-could-do

## Presentation

Rails 3.2.3 Can…

### Console
custom rake tags for help

`rails c -- sandbox` 

rails c has access to helper global variable
`helper.number_to_currency`

SASS for config of plugins

### Database
rails g resource user name:uniq email:string:uniq token:string{6} site:belongs_to

`rake db:migrate:status`

Serializer#load; Serializer#dump

User.pluck(:email)

rails g resource event article:belongs_to trigger

Allow You to Override Associations in Active Record

User.instantiate("id" => 2, 'email' => 'james@example.com')

Unlimited string for Postgresql

rails g resource article subject body:text

t.column :search, "tsvector"  # Take a look at this for Postgresql

different databases

### Ruby Extensions

Write Files Atomically awesome! 

File#write_atomic
Hash#deep_merge
Hash#except
Hash#merge (replace)
Hash#reverse_merge (allow defaults to be overwritten)
String#inquery… "magic".inquery.magic?

### Views

Understand a shorter ERb Syntax – 
Use Blocks to Avoid Assignments in Views
content_tag_for(:div, @articles) renders array of divs with yielded inner_html_
ActiveRecord::Base#to_partial_path

	config.action_view.default_form_builder
	config.action_view.field_error_proc
	
### Controllers & Routesr
config.exceptions_app = routes (Routes is a Rack App… you can route 404s accordingly)
require 'admin_validator'

	constraints AdminValidator do
		mount Resque::Server, at: "admin/resque"
	end

Enumerator.new

require 'thread'; ::Queue is thread safe

### Publish a Static Site Using Rails

Three hacks and you can rsync your site.

## Take Away

Drinking from the firehose.

"Crafting Rails Applications"
http://speakerdeck.com/u/jeg2