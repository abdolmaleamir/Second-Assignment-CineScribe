The CineScribe project is a Java application that utilizes two main classes, Actors and Movie, to fetch and display information about actors and movies. The project contains a simple text-based menu system that allows users to look up an actor or a movie by name. The application fetches data from two different APIs, one for actor information and another for movie information.

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