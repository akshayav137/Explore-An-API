# Which Dog Are You? 🐾

Which Dog Are You? is an interactive personality test that correlates the personality of the user with a certain dog breed through answers provided to five questions. Once the personality type of the user is calculated, the application sends an HTTP request to the Dog CEO API with the help of `fetch()` in JavaScript. In response, the API gives back the JSON object that contains the URL of a randomly chosen image of the dog of the correlated breed, which is then used to display the image. Since the image is being obtained by the request sent to the API, the user can get a different image even after taking the same quiz again. There was no API Key that was required for my specific project and no key was used. 

## API

This project uses the Dog CEO API:
`https://dog.ceo/dog-api/`

The project uses breed and sub-breed image endpoints such as:
`https://dog.ceo/api/breed/husky/images/random`
and
`https://dog.ceo/api/breed/retriever/golden/images/random`

The API response is returned as a JSON. The `message` property contains the dog image URL and the `status` property shows whether the request was successful or not.



## How to Run

1. Download or clone this repository.
2. Open the project folder in VS Code.
3. Open `index.html`.
4. Open the file in a browser or use the VS Code Live Server extension.
5. Answer all five personality questions.
6. After the final question, the application will determine your dog personality and retrieve an image from the Dog CEO API.
7. Click **Retake Quiz** to try again.

## Features

* Five-question interactive personality quiz
* Five possible dog personality results
* Dynamic scoring based on user answers
* Dog images retrieved from a public API
* Random images can change between quiz attempts
* Loading message while the API request is running
* Error handling for unsuccessful API requests
* Retake quiz functionality
* Responsive web design

## Error Handling

The API request uses a `try/catch` block and checks the HTTP response before attempting to display the image. If the request fails or the user loses their internet connection, the page displays a helpful error message instead of crashing.
