*A Migration is a file that keep track of changes to out database schema (structure of our database)*
### Why using migrations?
+ Mistakes to out database schema are very expensive to make. The entire app can go down, so we need to :
  + Quickly roll back changes
  + Test changes before we make them
+ Migrations could offer version countrol on database schema
### What migrations could do?
Stack migrations together to:
+ upgrade database schema
+ roll back database schema to a former version by reverting migrations applied
