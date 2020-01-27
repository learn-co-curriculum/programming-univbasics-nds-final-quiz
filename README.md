# Quiz: Nested Data Structures Final

???

# Nested Data Structures Final Quiz

For the following questions, use this data structure

```ruby
results = {
  :race_name => "Kentucky Derby",
  :year => 2019,
  :winners => [
    {
      :horse_name => "Country House",
      :trainer => "William I. Mott",
      :margin => 1.75
    },
    {
      :horse_name => "Code of Honor",
      :trainer => "Claude R. McGaughey",
      :margin => 2.5
    },
    {
      :horse_name => "Tacitus",
      :trainer => "William I. Mott",
      :margin => 3.25
    }
  ]
}
```

?: Which command will return "2019"?

( ) 
```
results[0]
``` 
( ) 
```
results[0][:year]
``` 
( ) 
```
results["Kentucky Derby"][:year]
``` 
(x) 
```
results[:year]
```

?: Taking into consideration both the previous hash of horse information 
and the method below, which line of code should we add at the "??" marker to **return a Hash** whose
`:horse_name` value matches the `sought_name` that's passed into
`find_horse_by_name`?

```ruby
def find_horse_by_name(sought_name)
  horse_result = nil
  i = 0
  while i < results[:winners].length do
    # ?? What Goes Here ??
    i += 1
  end
  horse_result
end
```

( ) `horse_result == results[:winners][i] if results[:winners][i][:horse_name] = sought_name` ( ) `horse_result == results[:winners][i] if results[:winners][i][:horse_name] == sought_name` (X) `horse_result = results[:winners][i] if results[:winners][i][:horse_name] == sought_name` ( ) `horse_result = results[:winners][i][:horse_name] if results[:winners][i][:horse_name] == sought_name`

?: What would be the result of this code?

```ruby
  i = 0
  coll = []
  while i < results[:winners].length do
    coll << results[:winners][i][:trainer]
    i += 1
  end
  p coll.length #=> ?
```

( ) nil ( ) 2 (X) 3 ( ) 4

?: What would be the result of this code?

```ruby
  i = 0
  coll = []
  while i < results[:winners].length do
    coll << results[:winners][i][:trainer]
    i += 1
  end
  coll #=> ?? What goes here ??
```

(X) `["William I. Mott", "Claude R. McGaughey", "William I. Mott"]` ( ) `2` ( ) `3` ( ) `["William I. Mott", "Claude R. McGaughey"]`

?: The `results` structure is a/an:

( ) `Hash` of `Array` ( ) `Array` of `Hash` (X) `Hash` ( ) `Array`

?: The `results[:winners]` structure is a/an:

( ) `Hash` of `Array` (X) `Array` of `Hash` ( ) `Hash` ( ) `Array`

?: We're preparing to code a looping algorithm to collect all the `:margin`s. Help us by retrieving the :margin of the **first** horse

( ) `results[:winners][1][:margin]` ( ) `results[:winners][-1][:margin]` ( ) `results[:winners][2][:margin]` (X) `results[:winners].first[:margin]`

?: We're preparing to code a looping algorithm to collect all the `:margin`s. Help us by retrieving the :margin of the **last** horse

( ) `results[:winners][1][:margin]` (X) `results[:winners][-1][:margin]` ( ) `results[:winners][2][:margin]` ( ) `results[:winners].first[:margin]`

?: The code `results[:winners][0] = results[:winners].first`  will test whether
the command `.first` operates like `[0]` when accessing an `Array`

( ) True (X) False

?: `results[:winners][-1] === results[:winners].last`

(X) True ( ) False

???
