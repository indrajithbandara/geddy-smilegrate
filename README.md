# Smilegrate
### Stop frowning during migrations!

Smilegrate is a simple command line utility for running migrations in Geddy.js.

It's used for simple migrations, like adding or removing a single column from a table.  Such a migration might be performed to add a table like so:

```
$ smilegrate add user string name
```

To add a row "name" of type "string" to the table "user".  Or, to remove the same row:

```
$ smilegrate remove user string name
```

Installation is a snap.  Just run `npm i -g smilegrate`.

## Under the hood

Smilegrate is basically performing three functions for you: 

- Generating a migration template using `geddy gen migration`.
- Populating that migration file with the bare minimum to perform what you requested.
- Running the migration using the `geddy jake db:migrate` command.
