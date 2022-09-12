# NetLogo

## Procedure
- Like function
    + change the word
    + report values / make judgement....( DO NOT change anything

## Var
- Agent var
    - build-in
    - user-defined
- Gloval var

- Local var
    - Define:
    ```
        let all-neighbors turtles-on neighbors
        // turtles ON the neighbors
        
        let similar-neighbors all-neighbors with [
            color = color-wanted
        ]
        // similar-neighbors := 
        // the tirtles within 'all-neighbors' of the same color as 'color-wanted'
    ```

## slef VS myself
- **slef**: like **this** in java
- **myslef**: the object that is of the upper layer

```
creat-turtles 1 [
    print self // turtle 0
    set color one-of base-colors
    ask neighbors4 [
        print self // a patch4
        set pcolor [ color ] of myself - 4 // myself: turtle0
    ]
]
```


## []

> If the argument is just an object, then it can be put there without []

> If the argument is a bunch of executed commens, we need [], for example:

```
to go
  if all? turtles [ demands-met? color ] [ stop ] // for each turtle, commands are executed
  .....
end
```

## Setup
- Always remember to **reset-ticks**
- **sprout-agent**: generate agent


## Set and let
- set: change values
```
    set culture replace-item selected-indice culture new-trait
```

- let: define new var


## Extensions
- Install extensions
    - Tools -> Extensions...
- Installed extensions
    - load
    ```
        extension [ nw ]
    ```

## hebavior space
- tool -> Behavior space -> new
- set the experiment

## create list
- [constant1 constant2 ... ]
- (list procedure1 procedure2 ... )
```
    (list [ -> update-weights ] [ -> update-state ])
```

## Reduce operator
- Transform list1 to one item
- reduce [ operator ] [ data ]

```
    reduce [ [a b] -> a + b ] [2 5 6 7 9]
    
    reduce + [ 2 5 6 7 9 ]
    
    reduce [ [a b] -> a sentence b ] [["a" 1] ["b" true] ["e" 23.4]]
    
    reduce sentence [["a" 1] ["b" true] ["e" 23.4]]
    
```

> We can define our own operation / functions in **to-report**, and just mention the name of the function reduce [operation] [data]**

## map
- Transform list1 to list2 with the same length

## filter VS with
- filter operate on list
```
    let indices-candidate filter [
      index -> item index [culture] of neighbor != item index culture
    ] range length culture
    
    show filter is-number? [1 "2" 3]
    => [1 3]
    show filter [ i -> i < 3 ] [1 3 2]
    => [1 2]
    show filter [ s -> first s != "t" ] ["hi" "there" "everyone"]
    => ["hi" "everyone"]
```
- with operate on agents
```
    let current-group turtles with [ label = groupID ]
```

































