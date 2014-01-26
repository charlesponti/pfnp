# Ruby

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
```