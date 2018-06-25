# Pattern Matching and Collection Types

## Pattern Matching
- `=` is __not__ an assignment operator in Elixir - it is a _match operator_
- `=` succeeds if Elixir can make the left-hand side equal the right hand side
- Elixir does permit _rebinding_ variables, but not until a matching process is complete
- To prevent rebinding, prefix the variable with `^`

### Try it out: 
- `a = 1`
- `1 = a`
- `2 = a`
- `i a`
- `a = 2`
- `i a`
- `[a, a] = [1, 2]`
- `[a, b] = [1, 2]`
- `[x, y, z] = [1, 2, 3]`
- `[1, a, 2] = [1, 4, 2]`
- `^a = 2`

## Data Collections
### Tuples
Tuples are fixed length collections, usually only 2-4 elements long.  
- `{25, 42}`
- `{"Bob", "White"}`

They are often used in returns, where the first value indicates success or failure of the operation and the second value contains a value. 
- `{:ok, "Bob White"}`
- `{:error, error_type}`


### Lists
Lists are collections of undetermined size. They are good for processing data linearly but not good for random access of data.
- `[1, 2, 3]`
- `["fuji", "granny smith", "winesap"]`

Technically, it's good to think of a list as having a `head` (the first value) and a `tail` (the rest of the list).  A list ends by linking to an empty list. 
- `[1, 2, 3]` === `[1]` -> `[2, 3]` === `[1]` -> `[2]` -> `[3]` -> `[]`

Lists come with their own set of operators: 
- `++`  Concatenate two lists: `[1,2] ++ [3,4] === [1,2,3,4]`
- `--`  Difference between two lists: `[1, 2, 3, 4] -- [2, 4] === [1, 3]`
- `in`  Membership in a list: `1 in [1, 2, 3] === true`

### Keyword Lists
Lists can use atoms as key words.  This is handy for passing optional parameters to functions. 
- `[name: "Bob White", city: "Nashville"] === [{:name, "Bob White"}, {:city, "Nashville}]`
- `userdata = [first_name: "Bob", last_name: "White", city: "Nashville"]`
- `userdata[:first_name] === "Bob"`

Another handy feature of Keyword Lists is that the keys do not have to be unique, which lets you pass in multiple values. 
- `style = [border: "1px", border: "solid", border: "#cccccc", padding: "10px"]`
- `Keyword.get_values(style, :border) === ["1px", "solid", "#cccccc"]`


### Maps
Maps are a collection of key-value pairs where each key is unique.  These collections are ideal for random access of data. The keys do not have to be the same type.
- `%{"AL" => "Alabama", "KY" => "Kentucky", "TN" => "Tennessee"}`
- `%{1 => "Tennessee", :abbr => "TN", "TN" = "Tennessee"}`

To access values in a map use bracket notation `[]`.  If the keys is an atom you may also use dot-notation. 
- `dinner = %{"fruit" => "blueberry", "vegetable" => "broccoli"}`
- `dinner["fruit"] === "blueberry"`
- `hexcolor = %{red: "#ff0000", green: "#00ff00", blue: "#0000ff"}`
- `hexcolor.red === "#ff0000"`
- `hexcolor[:green] === "#00ff00"`


### Structs

