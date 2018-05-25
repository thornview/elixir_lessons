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
- Tuples
- Lists
- Maps
- Keyword lists
- Structs

