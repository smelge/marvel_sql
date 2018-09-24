
The local cinema are having a Marvel Movie Marathon! They have asked you to help maintain their database of movies with times and attendees.

To access the database:

First, create a database called 'marvel'

# terminal
createdb marvel
Next, run the provided SQL script to populate your database:

# terminal
psql -d marvel -f marvel.sql
Use the supplied data as the source of data to answer the questions. Copy the SQL command you have used to get the answer, and paste it below the question, along with the result they gave.
Questions

Return ALL the data in the 'movies' table.

    SELECT * FROM movies

Return ONLY the name column from the 'people' table

    SELECT name FROM people

Oops! Someone at CodeClan spelled Keith's name wrong! Change it to reflect the proper spelling.

    UPDATE people SET name = 'Keith Douglas' WHERE id = 22

    22	Keith Douglas

Return ONLY your name from the 'people' table.

    SELECT * FROM people WHERE name = 'Tavy'

    Tavy Fraser

The cinema is showing 'Batman Begins', but Batman is DC, not Marvel! Delete the entry from the 'movies' table.

    DELETE FROM movies WHERE title = 'Batman Begins'

    8	Thor: The Dark World	2013	15:20
    10	Captain America: The Winter Soldier	2014	21:10

Create a new entry in the 'people' table with the name of one of the instructors.

    INSERT INTO people (name) VALUES ('Vince Hammerman')

    22	Keith Douglas
    23	Vince Hammerman

Pawel has decided to hijack our movie evening, Remove him from the table of people.

    He does not exist. He is a ghost.

The cinema has just heard that they will be holding an exclusive midnight showing of 'Avengers: Infinity War'!! Create a new entry in the 'movies' table to reflect this.

    INSERT INTO movies (title,year,show_time)
    VALUES ('Infinity War',2018,'00:00')

    19	Black Panther	2018	22:20
    20	Infinity War	2018	00:00

The cinema would also like to make the Guardians movies a back to back feature. Find out the show time of "Guardians of the Galaxy" and set the show time of "Guardians of the Galaxy 2" to start two hours later.

    SELECT title,show_time FROM movies WHERE title = 'Guardians of the Galaxy';
    UPDATE movies SET show_time = '18:20' WHERE title = 'Guardians of the Galaxy 2';

    15	Doctor Strange	2016	22:40
    16	Guardians of the Galaxy 2	2017	18:20
    17	Spider-Man: Homecoming	2017	18:10

Extension

Delete multiple entries from your table in a single command.

    DELETE FROM people WHERE id IN (19,23)

    18	Rana Akbar
    20	Thomas Gracie
    21	Xavier Godard
    22	Keith Douglas

Select all the movies ordered by year in descending order

    SELECT * FROM movies ORDER BY year DESC

    20	Infinity War	2018	00:00
    19	Black Panther	2018	22:20
    16	Guardians of the Galaxy 2	2017	18:20
    18	Thor: Ragnarok	2017	19:35
    17	Spider-Man: Homecoming	2017	18:10
    15	Doctor Strange	2016	22:40
    14	Captain America: Civil War	2016	14:45
    13	Ant-Man	2015	13:25
    12	Avengers: Age of Ultron	2015	23:00
    11	Guardians of the Galaxy	2014	16:20
    10	Captain America: The Winter Soldier	2014	21:10
    8	Thor: The Dark World	2013	15:20
    7	Iron Man 3	2013	21:55
    6	Avengers Assemble	2012	14:30
    5	Captain America: The First Avenger	2011	13:10
    4	Thor	2011	21:20
    3	Iron Man 2	2010	18:00
    2	The Incredible Hulk	2008	22:05
    1	Iron Man	2008	15:35
