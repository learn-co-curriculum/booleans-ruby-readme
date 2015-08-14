# Booleans and Comparisons

## Objectives

1. Review the concept of boolean values.
2. Use boolean operators and identify their return values.
3. Use comparison operators and identify their return values.

## Booleans

We've already learned a bit about the boolean (true-or-false) data type. In Ruby, a boolean refers to a value of either `true` or `false`, both of which are defined as their very own data types. Every appearance, or instance, of `true` in a Ruby program is an instance of `TrueClass`, while every appearance of `false` is an instance of `FalseClass`. 

For now, we don't need to understand the concept of classes in depth. Just know that classes serve as templates for Ruby objects. Think of `TrueClass` and `FalseClass` like cookie cutters––there is a `TrueClass` cookie cutter and a `FalseClass` cookie cutter and every appearance of `true` or `false` is like a cookie made with its respective cookie cutter. 

## Boolean Operators

How do we create boolean values in a Ruby program? Well, you can actually type `true` or `false` *or* we can write statements that *return* `true` or `false`. Now that we understand the concept of "truthiness"—that certain types of data are "truthy" and certain others are "falsey"—we can understand how to write such statements. 

We already know that Strings are one type of data that are truthy. Drop into IRB and use `!!` (the "double-bang operator") to determine that the string `"hi"` is truthy:

```ruby
!!"hi"
  #=> true 
```

In the next unit, we will learn how to use the native truthiness of data types like strings to write statements that return `true`. 

First, we're going to learn how to use **boolean operators** to write statements that return `true` or `false`.

### What are Boolean Operators? 

Boolean operators are really methods which means that they have return values. What do they return? `true` or `false` of course!

In Ruby there are three main boolean operators: 

* `!` ("single-bang") which represents "NOT", 
* `&&` ("double-ampersand") which represents "AND", and 
* `||` ("double-pipe") which represents "OR". 

For an `&&` ("and") to evaluate to `true`, both values of either side of the symbol must evaluate to `true`. For example: 

```ruby
true && true 
  #=> true

true && false
  #=> false
```
For an `||` ("or") to evaluate to `true`, only one value on either side of the symbol must evaluate to `true`. For example: 

```ruby
false || true
  #=> true
```
Finally, a `!` ("not") reverses the logical state of its operand: if a condition is `true`, then `!` will make it `false`; if it is `false`, then `!` will make it `true`. For example: 

```ruby
!true 
  #=> false

!false 
  #=> true
```

## Comparison Operators

To check if two values are equal, we use the *comparison operator* represent with `==` ("double-equal-sign"). If two values are equal, then the statement will return `true`. If they are not equal, then it will return `false`. For example: 

```ruby
1 == 1
 #=> true

1 == 7
 #=> false
```
**Top-tip:** *The comparison operator* `==` *is distinct from the assignment operator* `=` *that is used to set a variable equal to a value. Mistaking these for each other is a common cause of unexpected behavior.*

## Let's Practice!

Open up IRB and enter individually each of these lines below. Try to predict what the result will be before running it in IRB:

```ruby
true && true

false && true

1 == 1 && 2 == 1

"test" == "test"

1 == 1 || 2 != 1

true && 1 == 1

false && 0 != 0

true || 1 == 1

"test" == "testing"

1 != 0 && 2 == 1

"test" != "testing"

"test" == 1

!(true && false)

!(1 == 1 && 0 != 1)

!(10 == 1 || 1000 == 1000)

!(1 != 10 || 3 == 4)

!("testing" == "testing" && "Zed" == "Cool Guy")

1 == 1 && (!("testing" == 1 || 1 == 0))

"chunky" == "bacon" && (!(3 == 4 || 3 == 3))

3 == 3 && (!("testing" == "testing" || "Ruby" == "Fun"))
```

## More Comparison Operators 

Ruby is good at comparing things. For instance, it knows that `14` is larger than `3`. Let's see that in action.

```rb
14 > 3
  #=> true
```

Here, `14` is larger than `3`, so Ruby evaluates this to `true`. Comparisons in Ruby always evaluate to `true` or `false`.

The commonly used comparison operators are:

| Operator | Operation |
|:--------:|:----------|
| `==`     | If the values of the two the operands are *equal*, then the evaluation is `true`. |
| `!=`     | If the values of the two operands are *not equal*, then the evaluation is `true`. |
| `>`      | If the value of the left operand is *greater than* the value of right operand, then the evaluation is `true`. |
| `<`      | If the value of the left operand is less than the value of the right operand, then evaluation is `true`. |
| `>=`     | If the value of the left operand is *greater than or equal to* the value of the right operand, then the evaluation is `true`. |
| `<=`     | If the left operand is *less than or equal to* the value of the right operand, then the evaluation is `true`. |

Ruby can compare a lot more than just numbers. It can also compare strings:

```rb
"yellow" == "yellow"
  #=>true
```

And variables with known values:

```rb
my_mood = "happy"

my_mood == "happy"
 #=> true 
```

It can also compare variables against other variables:

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

Comparison operators are quintessential to developing logical flow.

 <div class="quiz-block">

 <div class='quiz-title'> <h1> Logical Operators Quiz</h1></div>

 <div class='question-block'> <p class='question-title'>`true && true`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`

</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`false && true`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`

</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`1 == 1 && 2 == 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`

</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`"test" == "test"`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`1 == 1 || 2 != 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`true && 1 == 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`false && 0 != 0`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`true || 1 == 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`"test" == "testing"`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`1 != 0 && 2 == 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`"test" != "testing"`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`"test" == 1`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`

</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`!(true && false)`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`

</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`!(1 == 1 && 0 != 1)`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`!(10 == 1 || 1000 == 1000)`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`!(1 != 10 || 3 == 4)`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`!("testing" == "testing" && "Zed" == "Cool Guy")`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`1 == 1 && (!("testing" == 1 || 1 == 0))`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0' class='answer'><span class='choice-index-span'>`true` </span><i class='fa fa-check-circle-o success-check'></i></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1'><span class='choice-index-span'>`false`
 
</span></div></form></div></div> <div class='question-block'> <p class='question-title'>`"chunky" == "bacon" && (!(3 == 4 || 3 == 3))`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`
 
</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div> <div class='question-block'> <p class='question-title'>`3 == 3 && (!("testing" == "testing" || "Ruby" == "Fun"))`</p>

 <div class='answer-block' data-question-type='multi_choice'><form class='question-form' accept-charset='UTF-8' method='post'> <div class='question-selection'><input id='multi-choice-0' type='radio' name='0' value='0'><span class='choice-index-span'>`true` </span></div> <div class='question-selection'><input id='multi-choice-1' type='radio' name='1' value='1' class='answer'><span class='choice-index-span'>`false`</span><i class='fa fa-check-circle-o success-check'></i></div></form></div></div>

 
</div>

test