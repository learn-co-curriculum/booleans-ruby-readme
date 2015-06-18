---
tags: readme
language: ruby
resources: 0
track: web development
topic: ruby
unit: control flow
lesson: booleans
---

# Booleans and Comparisons

## Booleans

* In Ruby there are three main boolean operators: `!` ("not"), `&&` ("and"), and `||` ("or"). These are really methods, which means they have return values. So what do they return? Only `true` or `false`.
  * For an and (`&&`) to evaluate to true, both values of either side of the double ampersand must evaluate to true.
  * For an or (`||`) to evalute to true, only one value on either side of the double pipes must evaluate to true.
  * Finally, a not (`!`) reverses the logical state of its operand. If a condition is true, then `!` will make it false and vice versa.


## Comparison Operators

* Open up IRB and type the non-commented portions of the code below. Try and predict what the result will be before checking with the comments or IRB:

```ruby
true && true
# => true
false && true
# => false
1 == 1 && 2 == 1
# => false
"test" == "test"
# => true
1 == 1 || 2 != 1
# => true
true && 1 == 1
# => true
false && 0 != 0
# => false
true || 1 == 1
# => true
"test" == "testing"
# => false
1 != 0 && 2 == 1
# => false
"test" != "testing"
# => true
"test" == 1
# => false
!(true && false)
# => true
!(1 == 1 && 0 != 1)
# => false
!(10 == 1 || 1000 == 1000)
# => false
!(1 != 10 || 3 == 4)
# => false
!("testing" == "testing" && "Zed" == "Cool Guy")
# => true
1 == 1 && (!("testing" == 1 || 1 == 0))
# => true
"chunky" == "bacon" && (!(3 == 4 || 3 == 3))
# => false
3 == 3 && (!("testing" == "testing" || "Ruby" == "Fun"))
# => false
```

## Comparisions

* Ruby is good at comparing things. For instance, it knows that 14 is larger than 3. Let's see that in action.

```rb
puts 14 > 3
#  └── true
```

* Here, 14 is larger than 3 so Ruby evaluates this to `true`. Comparisons in Ruby always evaluate to `true` or `false`.
* Here's a list of the commonly used comparison operators:

Operator               | Checks if the value of...
-----------------------|--------------------------------------------
==                     | two operands are equal or not, if yes then condition becomes true.
!=                     | two operands are equal or not, if values are not equal then condition becomes true.
>                      | left operand is greater than the value of right operand, if yes then condition becomes true.
<                      | left operand is less than the value of right operand, if yes then condition becomes true.  (a < b) is true.
>=                     | left operand is greater than or equal to the value of right operand, if yes then condition becomes true.
<=                     | left operand is less than or equal to the value of right operand, if yes then condition becomes true.

* Ruby can compare a lot more than just numbers. For instance, it can compare strings.

```rb
puts "yellow" == "yellow"
#  └── true
```

* It can also compare variables with known values.

```rb
arels_mood = "happy"

puts arels_mood == "happy"
#  └── true
puts arels_mood == "sad"
#  └── false
puts arels_mood == arels_mood
#  └── true
```

* It can also compare variables with other variables.

```rb
easter_eggs = 16
ducklings = 3

puts easter_eggs > ducklings
#  └── true
puts ducklings >= easter_eggs
#  └── false
puts ducklings == easter_eggs
#  └── false

# if you call class on a variable, you can see if it's a string, an integer, etc.
puts ducklings.class
#  └── Integer
puts easter_eggs.class
#  └── Integer
puts ducklings.class == easter_eggs.class
#  └── true
```


???

# Logical Operators Quiz

?: `true && true`

(X)`true` ( )`false`

?: `false && true`

( )`true` (X)`false`

?: `1 == 1 && 2 == 1`

( )`true` (X)`false`

?: `"test" == "test"`

(X)`true` ( )`false`
 
?: `1 == 1 || 2 != 1`

(X)`true` ( )`false`
 
?: `true && 1 == 1`

(X)`true` ( )`false`
 
?: `false && 0 != 0`

( )`true` (X)`false`
 
?: `true || 1 == 1`

(X) true () false
 
?: `"test" == "testing"`

( )`true (X)`false`
 
?: `1 != 0 && 2 == 1`

( )`true` (X)`false`
 
?: `"test" != "testing"`

(X)true ( )`false`
 
?: `"test" == 1`

( )`true` (X)`false`

?: `!(true && false)`

(X)`true` ( )`false`

?: `!(1 == 1 && 0 != 1)`

( )`true` (X)`false`
 
?: `!(10 == 1 || 1000 == 1000)`

( )`true` (X)`false`
 
?: `!(1 != 10 || 3 == 4)`

( )`true` (X)`false`
 
?: `!("testing" == "testing" && "Zed" == "Cool Guy")`

(X)`true` ( )`false`
 
?: `1 == 1 && (!("testing" == 1 || 1 == 0))`

(X)`true` ( )`false`
 
?: `"chunky" == "bacon" && (!(3 == 4 || 3 == 3))`

( )`true` (X)`false`
 
?: `3 == 3 && (!("testing" == "testing" || "Ruby" == "Fun"))`

( )`true` (X)`false`

 
???

