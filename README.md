# Syntax

## Objects

``` yaml
person: # person object has a list of key value pairs
    name: "Antony" # this is a string
    occupation: 'Engineer' # this is also a string
    age: 30 # this is a integer
    gpa : 4.2 # this is a floting point number
    fav_num: 1e+10 # this is a exponential number
    male: true
    birthday: 1999/12/23 18:19:20 # date is in ISO 8601 standard
    flaws: null # to show a null value
    hobies: # below is an example to create a list of values
        - running
        - movies
        - adventure
    movies: ["underworld", "fast & the furious"] # another syntax to create a list
    friends: # complex list eg) list of objects
        - name: "Sam"
          age: 32
        - {name: "Adam",age: 22} # another way
        -
         name: "James"
         age: 28
    description: >
        Description is the pattern of narrative development that aims to make vivid a place, object, character, or group. 
        Description is one of four rhetorical modes, along with exposition, argumentation, and narration. 
        In practice it would be difficult to write literature that drew on just one of the four basic modes
    # the above `>` syntax will ask yaml to render in a single line even though we have line breaks
    
```
