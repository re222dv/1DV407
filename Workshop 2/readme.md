# Boad Club Design

## Authors
- David Grenmyr
- Rasmus Eneman
- Sherief Badran

## Patterns
- Information Expert
- Dependency Injection
- MVC

## Languages
We chose to develop one program each. Two group members programmed in C# and one programmed in Dart. This
gave some interesting problems and findings.

## Problems/obstacles
One complication that occurred were that C# have multiple integer types with different length and Dart only
have one that grows to fit the number. This created problems when the C# versions read from the database after
the Dart one had written because the number type could be of different lengths.

When we chose that the entity classes Member and Boat should convert themselves from and to a generic JSON version
(Using Dictionaries/Maps, Lists and primitive types) to not bind them to a Mongo database, we could not find a way
for the C# version to convert the BsonDocument to generic objects as the Json.NET framework returned JObjects. And
thus the entities are dependent on Json.NET

Dart is an asyncronous language and thus the database library returns future results, Dart have an await keyword coming
however as it isn't done the Dart version of the program is forced to handle futures by for example using `Future.doWhile`
instead of simple `while` or `do while` loops. This makes the program harder to read and thus we have to conclude
that Dart, at least for now, isn't well suited for this kind of programs.
