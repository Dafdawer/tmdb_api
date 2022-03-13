# tmdb_api
Упражнение на чтение кода. Фильмы с TMDB

## An API for searching for personal recommendations in a personal movie DB 
Input a film name and find best matches in the local stored film database
(referred to as 'MDB' from now on, as opposed to the internet TMDB).
MDB itself is a little fragment of the internet-based [TMDB](https://www.themoviedb.org/)


**_How to use_**:
run
```
python3 [script_name]
```
Enter the path to the MDB, user API key or film's title to serve as a sample when
asked by a corresponding message.


### find_similar.py
The script asks for MDB path and a filmname (sample) to match results against.
Upon a successful search, the script goes through the MDB calculating each 
film's score and returns desired number of films (9 by default) having
highest score. This score is determined by comparing each MDB film's
parameters against sample ones and adding some value if they do match.


### hello_api_TMDB.py
As a test scripts asks for user API key and prints out "Saw II" film budget,
which is 4000000


### make_own_db.py
Asks for user API key and makes a copy of the first 1000 films data (or less
if not all requests are successful) from [TMDB](https://www.themoviedb.org/) and saves
it as a JSON file.


### own_db_helpers.py
Contains a method that takes a filepath as a parameter and turns its' content
into a python dictionary object. This script is meant for internal program use.


### search_in_db.py
Asks for MDB path and a keyword to search for. Makes a set of all movies in MDB
having the keyword in the name and prints it out in the alphabetical order.


### tmdb_helpers.py
The file contains internal API functions that take user API key and check if it's
valid, make request to the Russian part of [TMDB](https://www.themoviedb.org/?language=ru-RU)
(optional parametrs can be included, see [The Movie API Docs](https://developers.themoviedb.org/) for details).
Finally, the JSON recieved as response is returned as a Python file.
 
 
