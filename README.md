# tmdb_api
Упражнение на чтение кода. Фильмы с TMDB

## An API for searching a personal movie DB for personal recommendations


The program takes a sample movie and scans the designated film data base for films
having highest matches in parameters.The API consists of 6 files explained below.
**Install the requirements** by running
```
python3 -m pip install -r requirements.txt
```
**_How to use_**:
run
```
python3 [script_name]
```
Enter the path to the MDB, user API or film's title to serve as
a sample when asked by a corresponding message.


### find_similar.py


The script asks for the path to the movie database (MDB) and name of a film to match
results against (sample). Upon a successful search, the script goes through the MDB
calculating each film's rating score and returns desired number of films (9 by 
default) having highest rating. The score is calculated by comparing each MDB film's
parameters against sample ones and adding some value if they match. There are 4 
parameters: collection, genre, budget and original language. The rating gets 1000
in case 'collection' parameters match, 500 for genre, 300 for language and 100 for
budget. Thus one film can have a rating ranging from 0 to 1900. Finally, the
resulted list is printed in alphabetical order.


### hello_api_TMDB.py

As a test scripts asks for user API and prints out "Saw II" film budget,
which is 4000000


### make_own_db.py


Asks for user API and makes a copy of the first 1000 films data from internet-based 
[The movie database](https://www.themoviedb.org/) and turns it into a JSON object


### own_db_helpers.py


Contains a method that takes a path to a file as a parameter and turns the content
of the file into a python dictionary object. This file is meant for internal
program use.


### search_in_db.py


Asks for path to MDB and a keyword to search for. Makes a list of all movies in MDB
that have the keyword in the name and prints the list out in the alphabetical order.


### tmdb_helpers.py

The file contains internal API functions that take user API key and check if it's
valid, make request to the Russian part of [internet](https://www.themoviedb.org/)
(optional parametrs can be included, see 
[The Movie API Docs](https://developers.themoviedb.org/) for details). Finally,
the JSON recieved as response is turned into a Python dictionary object.
 
 
