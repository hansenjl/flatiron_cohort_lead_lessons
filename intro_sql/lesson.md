[Lesson Slides](https://docs.google.com/presentation/d/15aLQHxqCGXGCKc8BnhhRdlbKhGfC4atp37x6LcuUKkA/edit?usp=sharing)

### Live Coding Guide

#### Make your own table

Go to a good starting point:

In terminal:

```bash
sqlite3 people.db
```

```sql
CREATE TABLE people (id INTEGER PRIMARY KEY, name TEXT);
```

```sql
.quit
```
see new file:
```bash
ls
```
open the file back up
```sql
sqlite3
.open people.db
```
Make a new entry:
```sql
INSERT INTO people (name) VALUES ("Micah");
```
See the table
```sql
SELECT * FROM people;
```
Now, add some people from the study group

Open up DB browser, look at the database there

Run sql scripts:

`sqlite3 people.db < sql_playground/02_populate_table.sql`

#### Coding challenges

- use downloaded database: chinook.db.bak


## Challenges

1. Write the SQL to return all of the rows in the artists table?

```SQL
 SELECT * FROM artists;

```

2. Write the SQL to select the artist with the name "Black Sabbath"

```SQL
 SELECT * FROM artists WHERE name = "Black Sabbath";

```

3. Write the SQL to create a table named 'fans' with an autoincrementing ID that's a primary key and a name field of type text

```sql

```

4. Write the SQL to alter the fans table to have a artist_id column type integer?

```sql


```

5. Write the SQL to add yourself as a fan of the Postal Service? ArtistId **174**

```sql


```

6. Check out the [Faker gem](https://github.com/stympy/faker). `gem install faker`, open up irb, run `require 'faker'` and then generate a fake name for yourself using `Faker::Name.name`. How would you update your name in the fans table to be your new name?

   ```sql


   ```

7. Write the SQL to return fans that are not fans of the black eyed peas.

```sql


```

8. Write the SQL to display an artists name next to their album title

```sql


```

9. Write the SQL to display artist name, album name and number of tracks on that album

```sql


```

10. Write the SQL to return the name of all of the artists in the 'Pop' Genre

```sql


```

## BONUS (very hard)

11. I want to return the names of the artists and their number of rock tracks
    who play Rock music
    and have more than 30 tracks
    in order of the number of rock tracks that they have
    from greatest to least

```sql



```


## Key Vocabulary
- Select: selects attributes from a table(s)
- From references primary table we are querying
- Joins: adds a related table to our query
- On: How we set our relationship (primary key == foreign key)
- Where: Uses conditions to query data (non aggregate)
- Group: Allows us to base our query on groups of data
- Having: Uses aggregate functions to formulate conditions
- Order: Allows us to sort our data by an attribute in ASC and DESC order
- Limit: Allows us to query only an x number of data
- AS: Allows us to alias selected attributes by another name
