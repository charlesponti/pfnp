# Ruby

* a dynamic, general-purpose, object-oriented language created in 1995 by Yukihiro Matsumoto. He created Ruby with the explicit goal of making a programming language that is readable by humans and fun for developers to work with.

* As an object-oriented language, everything in Ruby is an object and belongs to class. A class is an object from which other objects can inherit and overwrite values and methods. For example, the number 2 is an object belonging to the Fixnum class. Fixnum, itself is an object, that extends from the Class class.

## Variables
```ruby
name = 'Sally'
```

## Loops
```ruby
10.times do
	puts "Hello World"
end
```

## Methods
```ruby
def add(x,y)
	x + y
end
```

* Ruby methods are like JavaScript function, in that they are simply executable code
* Unlike Javascript, you do not need to explicitly write return at the end of a method because Ruby automatically returns the value of the last executed expression within the method

## Class
```ruby
class Person
	def initialize(age,name)
		@age = age
		@name = name
	end
end

sally = Person.new(18, 'Sally Jones')

sally.age // 18
sally.name // 'Sally Jones'
```