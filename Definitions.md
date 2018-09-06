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
