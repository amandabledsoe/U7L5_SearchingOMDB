This my solution for Unit 7: Lab 5 "Searching OMDB" in the 2022 C# .NET After-Hours Boot Camp at Grand Circus.

# SEARCHING OMDB
### Objective: 
Consuming API Server-Side

### Task: 
Use the Open Movie Database API (Found here: http://www.omdbapi.com/ ) to Display movies to our view 

### What will the application do?
- When the user visits the site, they will be greeted with 2 buttons/links on the Index page. One will lead them to a movie search and the other will lead them to a Movie night page.
- The MovieSearch page will show off one movie
- The MovieNight page will show off multiple movies


### Build Specifications:
- Sign up with the API to obtain a key. Practice with the API in your browser, particularly searching by title. Familiarize yourself with the format of the data you get back.
- In your models folder, create a class to hold a single Movie based on what you saw playing with the API. (Tip: You only need to include the fields you’ll be using.)
- Create a new view in Views/Home called MovieSearch. Add an HTML form asking for the title of a movie to search for. Do not include method or action attributes on your form.
- Create two methods in the controller for searching for a movie, both of which will return the same view called MovieSearch: 
- MovieSearchForm() - [HttpGet] this will display the search form’s page. Set the form’s method to “post” and its action to the method described below. Have this return the view called MovieSearch.
- MovieSearchResults(string Title) - [HttpPost] this will be called when the search form is submitted. It will receive the title from the input on the page. Call the movie API, retrieve the JSON, return the results to the view. (Remember to pass both the view name and model!)
- Go back to the view and add the necessary @model declaration. After the form, include an if statement to determine if the model is not null, and if not, then display the movie information (including the poster, using an <img> tag).
- Create a new view called MovieNight. On this view allow the user to search by 3 Titles on the same form using separate inputs.
- Create two functions in the controller: 
- MovieNightForm() - [HttpGet] this will display the page, including a form with three inputs named Title1, Title2, and Title3. 
- MovieNightResults(string Title1, string Title2, string Title3) - [HttpPost] this will grab the titles from the input on the page. Call the API three times. Add each movie to a list and return the list to the view.
- Just as before, update your MovieNight view to include a model, an if statement checking if the model isn’t empty, and then a loop to display the three movies.

### Extra Challenges:
- Research bootstrap and add some bootstrap styling to your movie results. (Bootstrap is already installed on ASP.Net projects)
Add a genre search. 
- Hint: Not currently supported on omdbapi. You will need to find/create this information
