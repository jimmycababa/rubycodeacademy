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

  <!-- example of a histogram -->
  puts "Enter a phrase you'd like to analyze: "
text = gets.chomp

words = text.split

frequencies = Hash.new(0)

words.each { |word| frequencies[word] += 1 }

frequencies = frequencies.sort_by do |word, count|
  count
end

frequencies.reverse!

frequencies.each do |word, count|
  puts word + " " + count.to_s
end

<!-- friends here has a splat argument, which means that the method can receive on or more arguments -->
def what_up(greeting, *friends)

<!-- Add a block after .each that multiplies each item by itself and puts the result to the console. -->
my_array = [1, 2, 3, 4, 5]
my_array.each do |num| puts num * num
end

<!-- Use .sort! to sort the fruits array in descending (that is, reverse) alphabetical order. -->
fruits = ["orange", "apple", "banana", "pear", "grapes"]
fruits.sort! do |firstFruit, secondFruit| secondFruit <=> firstFruit
end

<!-- After your .sort! call, add an if-else statement. If rev is true, call reverse! on arr, else return arr.

Keep your numbers array and the puts statement so that you can see your work in action! -->
def alphabetize(arr, rev = false)
arr.sort!

if rev == true
 arr.reverse!
else
 arr
end
end

numbers = [1, 3, 5]
puts alphabetize(numbers)

<!-- symbols are not strings.  -->
<!-- create a new variable symbols, and store an empty array in it. Use .each to iterate over the strings array. For each s in strings, use .to_sym to convert s to a symbol and use .push  to add that new symbol to symbols. print the symbols array -->
symbols = []
strings.each do |s| 
if s == strings
symbols.push(s.to_sym)
end
end
print symbols

<!-- Go ahead and print out just the titles of our movies using puts.(hint: use the .select method) -->
movie_ratings = {
  memento: 3,
  primer: 3.5,
  the_matrix: 3,
  truman_show: 4,
  red_dawn: 1.5,
  skyfall: 4,
  alex_cross: 2,
  uhf: 1,
  lion_king: 3.5
}
puts movie_ratings.select { |movie, rating| puts movie}

<!-- sample case statement -->

puts "What's your favorite language?"
language = gets.chomp

case language 
when "Ruby"
  puts "Ruby is great for web apps!"
when "Python"
  puts "Python is great for science."
when "JavaScript"
  puts "JavaScript makes websites awesome."
when "HTML"
  puts "HTML is what websites are made of!"
when "CSS"
  puts "CSS makes websites pretty."
else
  puts "I don't know that language!"
end

<!-- a night at the movies code example -->
movies = {
  Memento: 3,
  Primer: 4,
  Ishtar: 1
}

puts "What would you like to do?"
puts "-- Type 'add' to add a movie."
puts "-- Type 'update' to update a movie."
puts "-- Type 'display' to display all movies."
puts "-- Type 'delete' to delete a movie."

choice = gets.chomp.downcase
case choice
when 'add'
  puts "What movie do you want to add?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "What's the rating? (Type a number 0 to 4.)"
    rating = gets.chomp
    movies[title.to_sym] = rating.to_i
    puts "#{title} has been added with a rating of #{rating}."
  else
    puts "That movie already exists! Its rating is #{movies[title.to_sym]}."
  end
when 'update'
  puts "What movie do you want to update?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "Movie not found!"
  else
    puts "What's the new rating? (Type a number 0 to 4.)"
    rating = gets.chomp
    movies[title.to_sym] = rating.to_i
    puts "#{title} has been updated with new rating of #{rating}."
  end
when 'display'
  movies.each do |movie, rating|
    puts "#{movie}: #{rating}"
  end
when 'delete'
  puts "What movie do you want to delete?"
  title = gets.chomp
  if movies[title.to_sym].nil?
    puts "Movie not found!"
  else
    movies.delete(title.to_sym)
    puts "#{title} has been removed."
  end
else
  puts "Sorry, I didn't understand you."
end

<!-- one line if statements -->
puts "I love love" if true

puts 1 < 2? "One is less than two!" : "One is not less than two."

<!--  Write a loop that only puts the even values of my_array. (Bonus points if you use a one-line if!) -->
my_array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

my_array.each do |x| puts x % 2 == 0? x : nil
end

<!-- Use .upto to puts the capital letters "L" through "P".

(Make sure to use puts and not print, so each letter is on its own line!) -->
"L".upto("P") do |letter| puts letter
end

<!-- conditional assignment example -->
favorite_animal ||= "tiger"

<!-- Use .times and a block to puts the string "I'm a block!" five times -->
5.times do |x|
puts "I'm a block!"
end

<!-- yield example -->
def yield_name(name)
  puts "In the method! Let's yield."
  yield("Kim")
  puts "In between the yields!"
  yield(name)
  puts "Block complete! Back in the method."
end

yield_name("Eric") { |n| puts "My name is #{n}." }

yield_name("jimmy") { |n| puts "My name is #{n}!"}