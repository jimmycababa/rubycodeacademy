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

<!-- using the unless statement -->
hungry = false

unless hungry
  puts "I'm writing Ruby programs!"
else
  puts "Time to eat!"
end

<!-- if else statement with user input -->

print "Pleathe enter a thtring: " 
user_input = gets.chomp
user_input.downcase!

if user_input.include? "s"
  user_input.gsub!(/s/, 'th')
else "you did it with no s!"
puts "your new phrase is #{user_input}"
end

<!-- until loop - the loop breaks when counter is greater than 10. -->
counter = 1
until counter == 11
  puts counter
  counter = counter + 1
end

<!-- Add 1 to counter, then assign that new value back to counter.” This provides a succinct way of updating variable values in our programs. -->
counter += 1

<!-- “For the variable num in the range 1 to 10, do the following.” the three dots in the range tells Ruby to exclude to final number in the count - "go up to but don't include 10" -->
for num in 1...10

<!-- Write a for loop that puts the numbers 1 to 20, including 20 -->
for num in 1..20
puts num
end

<!-- write a loop where i = 20. subtract fo each loop and skip over the odd numbers. break if when its less then or equal to zero -->
i = 20
loop do
i -= 1
next if i % 2 != 0
print "#{i}"
break if i <= 0
end

<!-- odds = [1,3,5,7,9] -->
<!-- Use the .each method on the odds array to print out double the value of each item of the array. In other words, multiply each item by 2.Make sure to use print rather than puts, so your output appears on one line. -->
odds = [1,3,5,7,9]

odds.each do |item|
item *= 2
print "#{item}"
end