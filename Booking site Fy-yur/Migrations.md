**A Migration is a file that keep track of changes to out database schema (structure of our database)**
### Why using migrations?
+ Mistakes to out database schema are very expensive to make. The entire app can go down, so we need to :
  + Quickly roll back changes
  + Test changes before we make them
+ Migrations could offer version countrol on database schema

|             without migrations          |           with migrations         |
|-----------------------------------------|-----------------------------------|
|Creating and recreating the same tables  |create migration script that solves|           |in database even for minor changes.      | differences between the old & new versions|
|Lose exisitng data in older tables       |Gives Fine-grain control to change existing tables|
|                                         | Auto-detects changes from the old & new version of the SQLALchemy|
### What migrations could do?
Stack migrations together to:
+ upgrade database schema
+ roll back database schema to a former version by reverting migrations applied
## Flask-Migrate
Flask-Migrate is an extension that handles SQLALchemy database migrations for flask applications using Alembic.
