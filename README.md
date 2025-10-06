# Ruby on Rails

## p, puts, print, variables, and reverse
```bash
address = [1,2,3,4,5,6,7,8]
```

```bash
p address 
```
This prints the address array.

```bash
new_address = address.reverse! 
```
The reverse! method will reverse data and destroy the original address with the new reversed one.

```bash
p new_address  
```
Print in new line, and `show quotes` signs of string.

```bash
new_address2 = address.reverse
```
Meanwhile the reverse only reverse the address and save it in new_address2 but the original address remains the same as before.

```bash
print new_address2
```
`No quote signs,` Print everything in only `1 line` without giving a newline.

```bash
puts new_address2
```
Print each item of array in `newline` and in `1 line` when a single string. `No quotes`.


#### Variables Declaration

No need to use `let, var etc`. For `const` we declare the variable by first letter as Capital or ALL-CAPS `Address or ADDRESS`
```bash
Address = [1,2,3,4,5]
OR
ADDRESS = [1,2,3,4,5]
```

#### About Return

Everything in Ruby always returns something, except `puts` and `print` which returns `nil`.
```bash
print 'hello'
Output: hello
=> nill
```
```bash
puts 'hello'
Output: hello
=> nill
```
```bash
p 'hello'
Output: "hello"
=> "hello"
```

## Function Definition

```bash
def hello_function  #Function defined
 puts "hello world"
end                #Function ended

hello_function     #Function called

output: hello world
=> nil
```
This is how you define and call a function in ruby.

```bash
def hello_function(something_to_say)     # something_to_say is a parameter
 puts something_to_say
end                

hello_function "Say Hi"
OR
hello_function("Say Hi")

output: Say Hi
=> nil
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
```bash

```
```bash

```

   