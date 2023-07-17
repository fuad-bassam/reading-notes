# Routing and Navigation Properties

so we took today about Routing and Navigation Properties and how we can link the table and make a relation between entities and we use some lambda expression.

so first of all we had 3 types of relation 

1. `1:1`: in this case we implement the table from the first model in the second model and do the reverse or we can use the first model a primary key as foreign key in the second one and the reveres for the second model 
2. `1:m or m:1` : in this relation we pass a list of the many parts inside the one part.
3. `m:m`: we create a join model have the keys for both models in the relation and do as we do in the `1:m` relation in both models but we do it for the join model.

for **Composite Key** : we make it by adding inside `DbContext` -> `OnModelCreating` -> we create `modelBuilder`

