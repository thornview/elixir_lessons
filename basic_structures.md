# A Few Basics
## Data Types in Elixir

|type|description|example
|string|a string| "Hi there"|
|integer|whole numbers | 25, 64|
|float|decimals| 3.141 |
|boolean| true/ false| true, false|
|atom|a constant whose name is its value|:error, :tree|
|tuple|collections of known size|{:ok, "Hello"}, {1, 2, 3}|
|list|collection of unknown size|["a", "b"], [1, 2]|
|map|an associative array|%{name: "Bob", number: "12"}, %{12 => "Eggs"}|
|nil|empty value| nil|

Technically, true, false and nil are the atoms :true, :false, and :nil

## Operators
|operator|description|example|
|=|a match operator that succeeds if Elixir can make the left side equal to the right side|list = [1,2,3], [a,b,c = list]|
|++|concatenate two lists|[1,2] ++ [3,4]|
|<>|concatenate two strings|"Hi, " <> "there"|
|and|'and' with booleans||
|or|'or' with booleans||
|&&|'and' with "truthy" values||
|\|\|or with "truthy" values||