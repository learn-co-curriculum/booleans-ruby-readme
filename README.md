# Booleans and Comparisons

## Objectives

1. Understand the concept of Boolen values
2. Learn how to use boolean operators and understand what their return values are
3. Learn how to use comparison operators and understand what their return values are

## Booleans

We've already learned a bit about the boolean (true/false) data type. Boolean refers to the values of `true` and `false` which are their very own data types in Ruby. Every appearance, or instance, of `true` in a Ruby program is an instance of TrueClass. Every appearance of `false` in a Ruby program is an instance of FalseClass. 

For now, we don't need to understand the concept of classes in depth. Just know that classes serve as templates for Ruby objects. Think of TrueClass and FalseClass like cookie cutters––there is a TrueClass cookie cutter and a FalseClass cookie cutter and every appearance of `true` or `false` is like a cookie made with the respective cookie cutter. 

## Boolean Operators

How do we create boolean values in a Ruby program? Well, you can actually type `true` or `false` *or* we can write statements that *return* `true` or `false`. Now that we understand the concept of "truthiness"––i.e., that certain types of data are "truthy" and certain others are "falsey"––we can understand how to write such statements. 

We already know that Strings are one type of data that are "truthy". Drop into IRB and use the `!!`, double bang operator, to determine that in fact, the string `"hi"` is "truthy":

```ruby
!!"hi"
  #=> true 
```

In the next unit, we will learn how to use the native "truthiness" of data types like strings to write statements that return `true`. 

First, we're going to learn how to use **boolean operators** to write statements that return `true` or `false`.

### What are Boolean Operators? 

Boolean operators are really methods. That means they have return values. What do they return? `true` or `false`!

* In Ruby there are three main boolean operators: `!` ("not"), `&&` ("and"), and `||` ("or"). 
  * For an and (`&&`) to evaluate to true, both values of either side of the double ampersand must evaluate to true. For example: 

  ```ruby
  true && true 
    #=> true

  true && false
    #=> false
  ```
  * For an or (`||`) to evalute to true, only one value on either side of the double pipes must evaluate to true. For example: 

  ```ruby
  false || true
    #=> true
  ```
  * Finally, a not (`!`) reverses the logical state of its operand. If a condition is true, then `!` will make it false and vice versa. For example: 

  ```ruby
  !true 
    #=> false

  !false 
    #=> true
  ```

## Comparison Operators

To check if two values are equal, we use the *comparison operator*, `==`. If two things are equal, the statement will return `true`. Otherwise, it will return `false. For example: 

```ruby
1 == 1
 #=> true

1 == 7
 #=> false
```
*This is different from the `=` that we use to set a variable equal to a value. 

## Let's Practice!

Open up IRB and type the non-commented portions of the code below. Try and predict what the result will be before checking with the comments or IRB:

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

## More Comparison Operators 

Ruby is good at comparing things. For instance, it knows that 14 is larger than 3. Let's see that in action.

```rb
14 > 3
  #=> true
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
"yellow" == "yellow"
  #=>true
```

* It can also compare variables with known values.

```rb
my_mood = "happy"

my_mood == "happy"
 #=> true 
```

* It can also compare variables with other variables.

```ruby
easter_eggs = 16
ducklings = 3

easter_eggs > ducklings
  #=> true
ducklings >= easter_eggs
  #=> false
ducklings == easter_eggs
  #=> false

# if you call class on a variable, you can see if it's a string, an integer, etc.
ducklings.class
  #=> Integer
easter_eggs.class
  #=> Integer
ducklings.class == easter_eggs.class
  #=> true
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

(X)`true` ( )`false`
 
?: `"test" == "testing"`

( )`true` (X)`false`
 
?: `1 != 0 && 2 == 1`

( )`true` (X)`false`
 
?: `"test" != "testing"`

(X)`true` ( )`false`
 
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

