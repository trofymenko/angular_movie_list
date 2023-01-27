# Movie List

## API to hit

*JSON API URL :*
`https://jsonmock.hackerrank.com/api/moviesdata?Year={input}`

## Expected Outputs 

- `No Results Found` 

## Environment 

- Angular CLI Version: 10.0.4
- Angular Core Version: 10.0.4
- Node Version: v14(LTS)
- Default Port: 8000

## Application Demo:

![](https://hrcdn.net/s3_pub/istreet-assets/b7veN-5seSkLqNKkQJrmXg/movie-list.gif)

## Functionality Requirements

The component must have the following functionalities:

- The input should initially be empty. The user can type a year into this input box to search for movies released in that year.

- Clicking on the `Search` button should make an API GET call to the URL `https://jsonmock.hackerrank.com/api/moviesdata?Year={input}` using the Angular HttpClient module. Here, {input} is the number entered into the text box. For example, for the value 2015, the API hit has to be `https://jsonmock.hackerrank.com/api/moviesdata?Year=2015`. 

- The response contains a data field, where data is an array of objects, and each object is a movie record.  A sample data field for year `2015` is below:

```
  "data": [
    {
      "Title": "Maze Runner: The Scorch Trials",
      "Year": 2015,
      "imdbID": "tt4046784"
    },
    {
      "Title": "Into the Grizzly Maze",
      "Year": 2015,
      "imdbID": "tt1694021"
    }
  ]
```

- Each movie record contains a `Title` field. Retrieve all the movies from the response and, for each movie record, display the Title as `<li>{title}</li>` inside `<ul data-test-id="movieList"></ul>`, in the order they appear in the data field.

- If there are no movies returned for the year by the API, you must render `<div data-test-id="no-result">No Results Found</div>` instead, and this element must be visible only when the data field is an empty array. This div should not be rendered initially since no API has been hit yet.

- Please note that the input field accepts only numbers. Test cases take care of calling the API with valid input, so writing input validation is not required.

- For testing purposes, please use the following year values - `2015` and `2016`.

## Testing Requirements

- The input should have the data-test-id attribute `app-input`.

- The `Search` button should have the data-test-id attribute `submit-button`.

- The `<ul>` should have the data-test-id attribute `movieList`.

- The `No Results Found` div should have the data-test-id attribute `no-result`.

## Project Specifications

**Read Only Files**
- src/app/app.component.spec.ts
- src/app/movie-list/movie-list.component.spec.ts

**Commands**
- run: 
```bash
npm start
```
- install: 
```bash
npm install
```
- test: 
```bash
npm test
```
