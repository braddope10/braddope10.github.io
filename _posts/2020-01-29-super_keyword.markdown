---
layout: post
title:      "**Super Keyword**"
date:       2020-01-30 00:18:36 +0000
permalink:  super_keyword
---


What exactly is the super keyword in Ruby?

The super keyword is used when DRY (Don't Repeat Yourself) coding. It calls a method from the parent class when entering it under the same method in a different class.

For example, lets say you called super under method called stop_crying. Ruby will then try to find the same stop_crying method under the parent class and go up the ancestry chain.

When #stop_crying is found it will invoke the method wherever you put the super keyword. If no method is found under the same name it will give you NoMethodError.

Let me give you an example!

class Discipline
        def behave
                 puts "Hey! don't do that."
        end
end

class Jason < Discipline
       def behave
                2.times do
                super
                end
       end
end

jason = Jason.new
jason.behave

#=> "Hey! don't do that."
#=> "Hey! don't do that."
