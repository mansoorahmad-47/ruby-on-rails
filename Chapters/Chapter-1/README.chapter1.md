# Chapter 1: The Ruby Programming Language

## p, puts, print, variables, and reverse
```bash
address = [1,2,3,4,5,6,7,8]
```

```bash
p address 

# output:
# [1,2,3,4,5,6,7,8]
```
This prints the address array.
<br>
<br>


```bash
new_address = address.reverse! 
```
The `reverse!` method will reverse data and destroy the original address with the new reversed one.
<br>
<br>

```bash
p new_address  

# output:
# [8,7,6,5,4,3,2,1]
```
Print in new line, and `show quotes` signs of string.
<br>
<br>

```bash
new_address2 = address.reverse
```
Meanwhile the `reverse` only reverse the address and save it in new_address2 but the original address remains the same as before.
Reverse can work on strings too.
<br>
<br>

```bash
print new_address2

#output:
# [8,7,6,5,4,3,2,1]
```
`No quote signs,` Print everything in only `1 line` without giving a newline.
<br>
<br>

```bash
puts new_address2

# output:
# 8
# 7
# 6
# 5
# 4
# 3
# 2
# 1
```
Print each item of array in `newline` and in `1 line` when a single string. `No quotes`.
<br>
<br>
<hr>

#### Variables Declaration

No need to use `let, var etc`. For `const` we declare the variable by first letter as Capital or ALL-CAPS `Address or ADDRESS`
```bash
Address = [1,2,3,4,5]
# OR
ADDRESS = [1,2,3,4,5]
```
<hr>


#### About Return

Everything in Ruby always returns something, except `puts` and `print` which returns `nil`.
```bash
print 'hello'

# Output: hello
# => nill
```
```bash
puts 'hello'

# Output: hello
# => nill
```
```bash
p 'hello'

# Output: "hello"
# => "hello"
```

<hr>

## Function Definition

```bash
def hello_function  #Function defined
 puts "hello world"
end                #Function ended

hello_function     #Function called

# output: hello world
# => nil
```
This is how you define and call a function in ruby.
<br>
<br>

```bash
def hello_function(something_to_say)     # something_to_say is a parameter
 puts something_to_say
end                

hello_function "Say Hi"
# OR
hello_function("Say Hi")

# output: Say Hi
# => nil
```
<hr>

## Working with Strings

#### String Concatenation

```bash
firstname = "Mansoor"
lastname = "Ahmad"

puts firstname + lastname
puts firstname + " " + lastname

# output: 
# MansoorAhmad
# Mansoor Ahmad

```
<hr>

#### String Interpolation

```bash
puts "#{firstname} #{lastname}"

puts '#{firstname} #{lastname}'    # String interpolation doesn't work in single quoted commas

# output:
# Mansoor Ahmad
# #{firstname} #{lastname}
```
We use `double quoted commas` for String interpolation in ruby. It won't work in single quoted commas.

<br>
<br>
<hr>

#### Methods, How to find them

In ruby everything is an object.
```bash
"Mansoor".class        # We use .class to finding out datatype
fullname = 'Mansoor Ahmad'
fullname.class
10.class         # Even the 10 is an object in ruby
10.0.class

# output:
# String
# String
# Integer
# Float

```
`.class` is just like `typeof` from javascript. It shows the datatype of the variable.
<br>
<br>

```bash
firstname.methods          # For showing all the methods of the variable/datatype.
```
`.methods` is used when you want to know all the possible methods available for that datatype.
<hr>

#### Some common methods

```bash
10.to_s                    # Will convert this integer to a string
10.to_s.class              # This is called method chaining
firstname.length           # same as Javascript to show string/array/object/number etc etc length

# output:
# "10"
# String
# 7
```
We can do `method chaining` to use multiple methods at once.
<br>
<br>

```bash
firstname.empty?        # to check if it's empty like "" or not
"".empty?
"".nil?                 # false, because in ruby everything returns something, so it can't be nil
nil.nil?

# output:
# false
# true
# false
# true
```
`.empty?` we use it to check either the variable/object is empty or not. `.nil?` we use it to check if something is returning nil or not.
<br>
<br>

```bash
fullname.sub("Ahmad", "Khan")
sometext = "I live in Dir Colony. Dir Colony is a good place for living"
sometext.gsub("Dir Colony", "Islamabad")

# output:
# Mansoor Khan
# I live in Islamabad. Islamabad is a good place for living
```
`.sub` is used to replace a `single word` in a text. `.gsub` is used to change the `same word used in multiple places ` in the text.
<br>
<br>
<hr>

#### Variable Assignment

In ruby `variable assignment` doesn't work like other languages. For Example

```bash
fullname = "Mansoor Ahmad"
newfullname = fullname
puts fullname
puts newfullname

fullname = "Mansoor Ahmad Khan"

puts fullname                # Here the name will print Mansoor Ahmad Khan as it is changed to this
puts newfullname             # Here it will print still the Mansoor Ahmad only because this was not actually pointed to the fullname variable, but instead it's pointing to the location in memory of the before fullname value.

# output:
# Mansoor Ahmad
# Mansoor Ahmad
# Mansoor Ahmad Khan
# Mansoor Ahmad

```
In ruby if a variable is pointing to another variable, it's actually `pointing to the location in memory` of that and not actually the variable. So if you point a `variable2` to `variable1` and then change the value of variable1, the value of variable2 won't be changed because variable2 was pointed to the memory location of the data which was stored if variable1 before.
<br>
<br>
<hr>

#### Escaping

In ruby sometimes we need to escape some special characters in text which can cause some problems, using backslash `\`. Like single quotes inside single quotes `'My name is 'Mansoor Ahmad''`. This text will give an error so we can escape the inside commas.

```bash
'My name is 'Mansoor Ahmad''             # This will give an error
'My name is \'Mansoor Ahmad\''         ' # Now using backslash We are escaping the comma after every slash to avoid errors. Note: Ignore the last quotation mark as in Readme.md file without this the comment was showing as a command.

# output:
# error
# "My name is 'Mansoor Ahmad'"
```
<br>
<br>

If you notice while using this code
```bash
'My name is #{fullname}'

# output:
# "My name is \#{fullname}"
```
You definitely will get the output like this `My name is \#{fullname}`. As single quotes doesn't support interpolation. Same we can do with double quotes too, by using backslash to escape special characters.

<br>
<br>

```bash
"My name is #{fullname}"
"My name is \#{fullname}"         #Used backslash for escaping the special character

# output:
# My name is Mansoor Ahmad
# My name is \#{fullname}

```
You can see we can use backslash for escaping any special character we want.
<br>
<br>
<hr>

#### Getting input from user

We use `gets.chomp` to get a string from user. Remember it will be a string only.

```bash
puts "What is your first name?"
firstname = gets.chomp
puts "What is your last name?"
lastname = gets.chomp
puts "Add a number to multiply it with 2"
number = gets.chomp

puts "Your first name is #{firstname} and your last name is #{lastname}"
puts number.to_i * 2                        # You have to convert the string to integer otherwise it will do concatenation

# output:
# Your first nameis Mansoor and your last name is Ahmad
# product of input number and 2
```
Here we used `.to_i` to convert the given number by user to integer, as `gets.chomp` can take strings only.
<br>
<br>

```bash
puts "Enter your first name?"
firstname = gets.chomp
puts "Enter your last name?"
lastname = gets.chomp

puts "Your full name is #{firstname} #{lastname}"
puts "Your full name reversed is #{lastname.reverse} #{firstname.reverse}"
puts "Your name has #{firstname.length + lastname.length} characters in it"

# output:
# Your full name is Mansoor Ahmad
# Your full name reversed is damhA roosnaM
# Your name has 12 characters in it

```
<br>
<br>
<hr>

## Working with Numbers

```bash
10/2
10/4                       # It will give 2 as answer because nominator and denominator both are integers and not float
10.0/4                     # Converting any one out of nominator and denominator to float will work
10/4.0
10/4.to_f                  # Or you can directly use the .to_f to convert the integer to float

# output:
# 5
# 2
# 2.5
# 2.5
# 2.5
```
For division it is necessary to use float for float output.
<br>
<br>
<hr>

```bash
"5" * "5"
"5" * 5
"-" * 20
2 * "5"
20.times {print "-"}
20.times {puts rand(10)}           # Print 20 random numbers from 0 to 9
rand
rand(100)                          # Print a random number from 0 to 99                  
'hello'.to_i                       # Will print 0

output:
error
55555
--------------------
error
--------------------
random numbers from 0 to 10  20 times
a random number
a random number from 0 to 99
0


```
```bash

```
```bash

```
```bash

```
```bash

```
```bash

```
<!-- 
```bash

```
```bash

```
```bash

```
```bash

```
```bash

```
```bash

```

    -->