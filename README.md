# Syntax

## Objects

``` yaml
person: # person object has a list of key value pairs
    name: &name "Antony" # this is a string
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
    code: |
        echo "Example to show the formatting is preserved"
        curl http://www.google.com
        echo "we can just take this bash script bloack and execute it"
    # we can look at anchoring
    id: *name # if the name is updated then id will also be updated
    # complex anchoring
    base: &complex
        variable1: "val"
    base2:
        <<: *complex # this will insert variable1: "val" here
        val2: "val2"
    floating_age: !!float 23 # this will be interpreted as 23.0
    string_gpa: !!str 4.2 # this will be rendered as string
```
