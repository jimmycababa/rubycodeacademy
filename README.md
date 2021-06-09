<!-- ruby tutorial -->

<!-- returns the length of the string. puts shows in the console -->
puts "jimmy".length

<!-- coverting strings to uppercase and lowercase -->
puts "jimmy".upcase
puts "jimmy".downcase

<!-- commenting -->
<!-- "hello" #hi -->
<!-- the '#' symbol is how we comment out code -->
<!-- =begin and =end is another way to comment. everything in between those expressions will be commented out -->

<!-- first program written. gets.chomp removes the space that ruby autonatically adds. capitalize! capitalizes the first letter and leaves the rest lowecase. #{} is called string interpolation, which takes the assigned variable and puts it in the string where you want it -->

print "What's your first name?'"
first_name = gets.chomp
first_name.capitalize!

print "What's your last name?"
last_name = gets.chomp
last_name.capitalize!

print "What city do you live in?"
city = gets.chomp
city.capitalize!

print "What state are you from?"
state = gets.chomp.upcase
state.upcase!

puts "Your first name is #{first_name} and your last name is #{last_name}. You are from #{city}, #{state}."