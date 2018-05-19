# Getting Started

## Why Functional Programming
* Concurrency is difficult in OOP
* CPUs aren't getting faster, they are getting more cores
* Distributed computing is becoming more common
* Functional programming is designed to support concurrency

## Thinking Differently
* _"The problem with a completely new programming paradigm isn't learning a new language. ... The tricky part is learning to __think__ in a different way."_ - Neal Ford
* _"OO makes code understandable by encapsulating moving parts.  FP makes code understandable by minimizing moving parts"_ - Michael Feathers
* _"Imperative programming focuses on __how to solve a problem__, describing each step as actions. ... Declarative programming focues on __what is necessary to solve a problem__."_ - Ulisses Almeida

## Some Key Concepts of Functional Programming
* All values are immutable
* Functions are basic building blocks
* The code is declarative (focus on "what" instead of "how", ie - "Here's my list, here's the filter" instead of "Here's the list.  Now, take the first item, compare it to the filter, decide if matches, then do this with it, then get the next value ... etc.")


# Playing with Elixir
## Some Syntax
The tables below introduce data types and operators for Elixir. Use IEX and these tables to do the exercises below. 

## Data Types in Elixir
|type|description|example
|---|---|---|
|string|a string| "Hi there"|
|integer|whole numbers | 25, 64|
|float|decimals| 3.141 |
|boolean| true/ false| true, false|
|atom|a constant whose name is its value|:error, :tree|
|tuple|collections of known size|{:ok, "Hello"}, {1, 2, 3}|
|list|collection of unknown size|["a", "b"], [1, 2]|
|map|an associative array|%{name: "Bob", number: "12"}, %{12 => "Eggs"}|
|nil|empty value| nil|

Technically, _true_, _false_ and _nil_ are the atoms :true, :false, and :nil

## Operators
|operator|description|example|
|---|---|---|
|=|a match operator that succeeds if Elixir can make the left side equal to the right side|list = [1,2,3], [a,b,c = list]|
|==|check if two values are equal| 1 == 1.0|
|!=|check if two values are not equal| 1 != 1.0|
|++|concatenate two lists|[1,2] ++ [3,4]|
|<>|concatenate two strings|"Hi, " <> "there"|
|and|'and' with booleans| true and 1|
|or|'or' with booleans|true or false|
|&&|'and' with "truthy" values (_false_ and _nil_ are "falsey" values)|nil && 2|
|\|\||or with "truthy" values|nil \|\| 2|

# Exercises
1.  Does `1 == 1.0`?
2.  Does `"1" == 1`?
3.  Does `:dog == "dog"`?
