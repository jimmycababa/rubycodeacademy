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

<!-- .split takes in string and returns an array. if we pass it a bit of text in parentheses it will divide the string wherever it sees that bit of text, called a delimiter. -->
<!-- this example of split will take the string text and split it whenever it sees a comma -->
text.split(",)  


puts "enter something"
text = gets.chomp

puts "enter words to be redacted"
redact = gets.chomp

words = text.split(" ")

words.each { |letter|
if letter == redact
print "REDACTED "
else
print letter + " "

end}

<!-- multidimensional array. this one is a 2 dimensional array -->
my_2d_array = [["hi"],["there"],["fartface]]

<!-- accessing hash values -->
pets = Hash.new
pets["wynter"] = 'dog'

puts pets["wynter"]

<!-- iterating over an array with each. It is saying that we take this array and for each element, print it to the console. -->
languages = ["HTML", "CSS", "JavaScript", "Python", "Ruby"]
languages.each{ |butt| puts butt}

<!-- we want to iterate over s in such a way that we don't print out each elemenet as an array, but each element as a sub array. so we iterate through .each element in the array (sub_array). then we iterate through .each sub_array and puts out their items-->
s = [["ham", "swiss"], ["turkey", "cheddar"], ["roast beef", "gruyere"]]
s.each do  |sub_array| sub_array.each do |x| puts x
end
end

<!-- iterating over hashes -->
<!-- use .each to iterate over the hash. use puts to print each key-value pair, separated by a colon and a space. -->
secret_identities = {
  "The Batman" => "Bruce Wayne",
  "Superman" => "Clark Kent",
  "Wonder Woman" => "Diana Prince",
  "Freakazoid" => "Dexter Douglas"
}
  secret_identities.each do |hero, normal|
  puts "#{hero}: #{normal}"
  end

  