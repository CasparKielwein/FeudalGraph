# Graph

The relationship graph, like any graph, consists of nodes and edges.
Nodes represent people and organisations. Edges represent 1 to 1 relationships between people / organisations.

The whole relationship graph consists of several subgraphs which are of interest separate from each other.
The alliances and wars between Countries and the family tree of the ruling families are not independent but are interesting on their on.

A pair of nodes can be connected by more than one Edge.
The graph might consist of disjunct subgraphs.
Edges can but don't have to be directed.

## Nodes
* Person: A natural person within the setting
* Group: Any group of people within the Setting. Examples: Countries, Guilds, The Church.

## Edges
* *Is Part Of*: Node A {Person | Group} is part of Node B {Group}. Example: A person is a Member of the Church. A Principality is part of a Kingdom
* *Child* Node A {Person} is the child of Node B {Person}
* *Married* Node A {Person} is married to Node B {Person}
* *Rules* Node A {Person} rules Node B {Group]. Since we model a feudal society we assume that each Group is rules by one Person.
* *Enemy* Node A {Person | Group} is an enemy of Node B {Person | Group}. 
* *Ally* Node A {Person | Group} is an ally of Node B {Person | Group}. 

## Assumptions
* A Person can only be the child of two Persons who must be married. (yeah I know...)
* A Person can only be married to exactly one other person.
* Two nodes can only be connected by either the *Ally* or *Enemy* relationships.
* A Group always has exactly one ruler.

# Abstract Concepts

Concepts and concrete entities realising these concepts are defines in toml. <https://github.com/toml-lang/toml>.
Each concept is defined as a section (in brackets).
Each concept has one array "values" of entities realising the concept.
Each entity is one String or an array of strings. All strings within a single array are considered to be synonyms of the same entity.
Entities can reference other concepts by including the name of the concept in curly braces.
Cycles of references are allowed.
If an entity has the value of another concept, the two are equivalent. Thus concepts can be entitites of other concepts.

```
[name_of_this_concept]
values = [ "name", ["name2", "synonym"]]
```
