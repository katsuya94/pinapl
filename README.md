# `pinapl`
`pinapl` Is Not A Programming Language

## Introduction
When creating large systems with complex specifications developers are impeded by limited knowledge of the system as a whole. This is a cause of...
* Code that is inconsistent with logical organization of the codebase
* Loss of modularity and consequently testability
* Lost development time attempting to understand the codebase
* Hard-to-find bugs
* Disassociation between code and the specifications it satisfies

Traditional solutions to these problems include...

* Heavy documentation
* Statically typed languages with strict object-oriented design
* Extensive code reviews
* Extensive testing

These solutions impose rigid restrictions upon developers. `pinapl` attempts to do the following...

* Maintain modularity of code
* Maintain separation of concerns
* Facilitate a complete understanding of systems and where any given piece of code fits in
* Strong association between code and specifications
* Provide a medium for specifying desired behavior with implementation in any language
* Provide tools for testing, configuring, running, and maintaining systems
* Allows developers to use multiple representations of a well-defined datatype

## Solution
`pinapl` is a specification language for the interlocking components that make up a system.

## Proof of concept
`scoreboard` is a web service for keeping track of and displaying scores for arbitrary games. It is implemented with three services...

* sqlite database
* Ruby Sinatra REST API for setting up games and adding/updating/retrieving scores
* Node.js/Express/AngularJS Web interface that hooks into the REST API

## Lifecycle of a `pinapl` command
```
pinapl exec <<- 'EOF'
(Database.insert "dogs" (object 'kind "shiba" 'name "doge" 'mood "much wow")) 
EOF
```

After evaluation of the `pinapl` expression, this becomes...

```
(object 'data 
```

## Random thoughts

`&::Thing` is how you address library modules
`~::Thing` is how you address local modules
