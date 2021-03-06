# Deprecated!

The long awaited event at least took place.

I've created the gem https://rubygems.org/gems/rspec_rails_scaffold_templates

It covers only scaffold functionality, as the rest does not need any change in rails.

If you are interested in more automation of you work I suggest to look also at other my gems https://rubygems.org/profiles/koulikoff

So, this project is not supported any more. ;-)

# Information about this fork

This for is no longer following the normal scaffolding layout of Rails.
It uses I18n backend for headings, model attributes names etc in it's views.

## Rails 4 HAML Scaffold Generator

Essentially just a copy of the Rails 4 ERB generator with HAML replacements for the templates.

Original idea from [Paul Barry's article on custom genrators][OriginalIdea]

### Installation

1. Generate your new rails application:

        rails ApplicationName
        cd ApplicationName

2. Edit "Gemfile" and add "gem haml" to the gem list
3. Either

        gem install haml

    ...or...

        bundle install

4. Edit config/application.rb and add the following:

        config.generators do |g|
            g.template_engine :haml
        end


5. Either

        git clone https://github.com/dima4p/rails4_haml_scaffold_generator.git lib/generators/haml

    ...or...

        git submodule add https://github.com/dima4p/rails4_haml_scaffold_generator.git lib/generators/haml
  
6. Create stuff with:

        rails generate controller ControllerName index
        rails generate mailer ExamplesNotifications
        rails generate scaffold FancyModel
    
    ... or if you like to mix it up with ERB, ignore step 5 and use ...

        rails generate haml:controller ControllerName index
        rails generate haml:mailer ExamplesNotifications
        rails generate haml:scaffold FancyModel

7. You can also add --cancan if you use the cancan authorization

        rails generate scaffold FancyModel <fields> --cancan

8. You can also add --simple_form if you use gem simple_form

        rails generate scaffold FancyModel <fields> --simple_form

[OriginalIdea]: http://paulbarry.com/articles/2010/01/13/customizing-generators-in-rails-3
