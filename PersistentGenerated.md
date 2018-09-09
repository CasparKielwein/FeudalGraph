Random generators for people, places etc. are backed up by a database of already generated objects.
As the database and thus the generated setting grows, the probability of taking an already existing object instead of generating a new one grows.

The database is filled lazily when attributes of existing objects are querried.
Example: A *Person* is generated. That person is from a *Place*. This *Place* and its name has now been generated and added to the database.
But there are no Attributes of it stored yet. When more information about the *Place* is querried, new data like additional people in it are generated.

This is essentially a wiki with procedurally generated content.
