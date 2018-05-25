# Getting Started

## Why Functional Programming
* Concurrency is difficult in OOP
* CPUs aren't getting faster, they are getting more cores
* Distributed computing is becoming more common
* Functional programming is designed to support concurrency

## Thinking Differently
* _"The problem with a completely new programming paradigm isn't learning a new language. ... The tricky part is learning to __think__ in a different way."_ - Neal Ford
* _"Imperative programming focuses on __how to solve a problem__, describing each step as actions. ... Declarative programming focuses on __what is necessary to solve a problem__."_ - Ulisses Almeida

## Some Key Concepts of Functional Programming
* All values are immutable
* Functions are basic building blocks
* The code is declarative (focus on "what" instead of "how", ie - "Here's my list, here's the filter" instead of "Here's the list.  Now, take the first item, compare it to the filter, decide if matches, then do this with it, then get the next value ... etc.")


# Playing with Elixir

## IEx
|command|description|
|---|---|
|i| __introspect__ - describe a value|
|h| __help__ - get documentation on something|
|__{Module}__.`<tab>`|List available functions in a module|

The `i` and `h` commands are functions.  In Elixir, functions can be called with or without parentheses. 

## Variables
* Variables are dynamic (you don't declare their type)
* Variables start with a lower case letter and may end with a `?` or `!`
* In Elixir, snake case variable names are preferred `this_is_snake_case`

## Elixir Basic Data Types
|type|description|example
|---|---|---|
|string|a string| "Hi there"|
|integer|whole numbers, which may use `_` to separate thousands | 25, 64|
|float|decimals| 3.141 |
|boolean| true/ false| true, false|
|atom|a constant whose name is its value|:error, :tree, |
|nil|empty value| nil|

Technically, _true_, _false_ and _nil_ are the atoms :true, :false, and :nil

## Operators
|operator|description|example|
|---|---|---|
|===|strict equality| 1.0 === 1.0|
|!==|strict inequality| 1.0 !== 1|
|==|value equality| 1 == 1.0|
|!=|value ineqality| 1 != 1.0|
|<>|concatenate two strings|"Hi, " <> "there"|
|and|'and' with booleans| true and 1|
|or|'or' with booleans|true or false|
|&&|'and' with "truthy" values (_false_ and _nil_ are "falsey" values)|nil && 2|
|\|\||or with "truthy" values|nil \|\| 2|

# Exercises
## Playing in IEx
Enter the following commands in IEx to explore the RPL interface
1. h
2. h(IEx)
3. h IO
4. Enum.`<tab>`
5. IO.`<tab>`
6. clear
7. i "dog"
8. i 24
9. i true

## Playing with Basic Data Types
1.  Does `1 == 1.0`?
2.  Does `"1" == 1`?
3.  Does `:dog == "dog"`?
4.  Does `1_000 === 1000`?
5.  Does `1,000 == 1_000`?
6. Which of the following expressions are valid?
  - `value = 1`
  - `Paycheck = 12_000`
  - `at_home? = :true`
  - `not_true! = true`
  - `"welcome " + "home"`
7.  Which of the following is false?  Which is illegal?
  * `nil || 0`
  * `false || nil`
  * `false && nil`
  * `false && 0`
  * `nil or 0`
  * `0 or false`
  * `nil && true`
8. According to Elixir, what is `2 + 1.141`?
9. What is equal to `:my_value`?

