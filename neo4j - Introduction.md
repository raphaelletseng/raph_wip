## neo4j and Graph Databases

#1. What is a graph database?
** Node + Relationships**
-A node can be a person, place, thing etc. 
-A relationship tells us how 2 nodes are associated

[Image](https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwi6-t_zppXkAhVcl48KHTP4Az4QjRx6BAgBEAQ&url=https%3A%2F%2Fneo4j.com%2Fblog%2Fwhy-graph-databases-are-the-future%2F&psig=AOvVaw35ZF0FXnl1G5ijJBqjbFvy&ust=1566522953071108)

Nodes can be **labelled** with multiple labels to make it easier to group them. 
You can add **properties** to nodes and relationships to add more information to the graph. 

#2. How do we query the graph?
neo4j uses **CYPHER**, a declarative query language to get information from the graph. 

-Eg. CREATE (:Label{Property})-[:RELATIONSHIP]->(Label{Property})
- CREATE (:Person{name: "Harry"}) -[:LOVES] (:Person {name: "Tom"})

neo4j supports java, JavaScript, Python, C# and Go drivers. 

#3. Creating a graph database

-CREATE (The Matrix: Movie {title: "The Matrix", released 1999, tagline: "Welcome to the Real World"})
-CREATE (Keanu: Person {name: "Keanu Reeves", born: 1964})
-CREATE (Keanu)-[:ACTED_IN{roles:"Neo"}) -> (The Matrix)

**Node**: A representation of a domain entity with labels, properties and relationships
-Generally: CREATE (optionalVariable: optionalLables {optionalProperties})

You can create multiple nodes by separating with a comma:
CREATE (:Person {name: "Michael Caine", born: 1933}), (:Person {name: "Liam Neeson", born: 1952}), (:Person {name: "Katie Holmes", born: 1978})

-**MERGE** will prevent the creation of a node with the same properties as a node that already exists (i.e duplicates)

-
