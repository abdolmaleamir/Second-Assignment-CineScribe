Celebrity and Movie Information Lookup
This project is a simple Java program that allows you to look up information about actors and movies using the Celebrity API and the OMDb API.

Description
This program allows you to search for information about actors and movies using their names. It uses the Celebrity API to retrieve actor information and the OMDb API to retrieve movie information. The program provides information such as the actor's net worth, date of death, and is alive status, and the movie's rating, release year, and actors.

Dependencies
Clone the repository to your local machine.
Navigate to the project directory in your terminal.
Run mvn clean install to build the project.
Executing program
Run java -cp target/movie-actor-lookup.jar Main to start the program.
Enter the name of an actor or a movie when prompted.
Help
If the program fails to retrieve data for a given actor or movie, make sure that the name is spelled correctly and try again.

Authors
amirhossein abdolmaleki


Classes and Methods
Main
The Main class is the entry point of the program. It creates instances of the Actors and Movie classes and provides a command-line interface for the user to interact with the program.

main
The main method is the entry point of the program. It creates instances of the Actors and Movie classes, and enters an infinite loop that prompts the user to choose an option, look up an actor or a movie, or exit the program.

Actors
The Actors class is responsible for retrieving and parsing actor information from the Celebrity API.

getActorData
The getActorData method retrieves the raw data for an actor from the Celebrity API. It takes an actor's name as a parameter and returns a string representation of the actor's data, or null if an error occurred.

getNetWorthViaApi
The getNetWorthViaApi method extracts the actor's net worth from the raw data. It takes the raw data as a parameter and returns the net worth as a double.

isAlive
The isAlive method extracts the actor's alive status from the raw data. It takes the raw data as a parameter and returns the alive status as a boolean.

getDateOfDeathViaApi
The getDateOfDeathViaApi method extracts the actor's date of death from the raw data. It takes the raw data as a parameter and returns the date of death as a string.

Movie
The Movie class is responsible for retrieving and parsing movie information from the OMDb API.

getMovieData
The getMovieData method retrieves the raw data for a movie from the OMDb API. It takes a movie's title as a parameter and returns a string representation of the movie's data, or null if an error occurred.

getRatingViaApi
The getRatingViaApi method extracts the movie's rating from the raw data. It takes the raw data as a parameter and returns the rating as a string.

getImdbVotesViaApi
The getImdbVotesViaApi method extracts the movie's IMDb votes from the raw data. It takes the raw data as a parameter and returns the IMDb votes as an integer.

getActorListViaApi
The getActorListViaApi method extracts the list of actors from the raw data. It takes the raw data as a parameter and returns the list of actors as a string.
The CineScribe project is a Java application that utilizes two main classes, 
Actors and Movie, to fetch and display information about actors and movies. The project contains a simple text-based menu system that allows users to look up an actor or a movie by name. The application fetches data from two different APIs, one for actor information and another for movie information.

The Actors class is responsible for fetching data about a specific actor by their name. It has a constructor that takes two arguments, a string representing the net worth and a boolean indicating if the actor is alive. The class contains several methods, including:

getActorData(name): Fetches the data for the specified actor from the API and returns the JSON string.
getNetWorthViaApi(actorsInfoJson): Parses the JSON string and returns the net worth of the actor as a double.
isAlive(actorsInfoJson): Parses the JSON string and returns a boolean indicating if the actor is alive or not.
getDateOfDeathViaApi(actorsInfoJson): Parses the JSON string and returns the date of death of the actor as a string.
The Movie class is responsible for fetching data about a specific movie by its title. It has a constructor that takes three arguments: an ArrayList of strings representing the actors, a string for the rating, and an integer for the IMDb votes. The class contains several methods, including:

getMovieData(title): Fetches the data for the specified movie from the API and returns the JSON string.
getImdbVotesViaApi(moviesInfoJson): Parses the JSON string and returns the IMDb votes as an integer.
getRatingViaApi(moviesInfoJson): Parses the JSON string and returns the rating as a string.
getActorListViaApi(movieInfoJson): Parses the JSON string and returns the list of actors as a string.
The Main class contains the main method, which initializes an instance of the Actors and Movie classes and handles user input. The main method presents the user with a simple text-based menu system, allowing them to look up an actor or a movie by name. The user's choice is passed as an argument to the respective method in the Actors or Movie class. The result is then displayed on the console.


In summary, the CineScribe project is a Java application that allows users to fetch information about actors and movies from two different APIs. The project contains two main classes, Actors and Movie, which handle the API requests and parse the JSON responses. The Main class provides a simple text-based menu system for user interaction. However, there are some compilation errors that need to be addressed for the project to run successfully

last thing that is necessary to add is the error that the program recieves when you try to insert a movie or an actor that doesnt exist in the api.
it is somehow related to gradle disfunction .





