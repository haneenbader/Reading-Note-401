# Room

The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

    Compile-time verification of SQL queries.
    Convenience annotations that minimize repetitive and error-prone boilerplate code.
    Streamlined database migration paths.


_Defining data using Room entities_

When you use the Room persistence library to store your app's data, you define entities to represent the objects that you want to store. Each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.

That means you can use Room entities to define your database schema without writing any SQL code.


Define relationships between objects

Because SQLite is a relational database, you can specify relationships between entities. Even though most object-relational mapping libraries allow entity objects to reference each other, Room explicitly forbids this. To learn about the technical reasoning behind this decision, see Understand why Room doesn't allow object references.

