# MovieAPP  https://tejaskarde21.github.io/MovieAPP/Movie/index.html

hello(): This function is called when a dropdown menu with the id selectinput changes. It checks whether the "movies" or "series" radio button is checked, and based on that, it adds an event listener to the respective category for either a change or a "rad" event. The event listener will call moviesearch() or seriessearch() with the selected value.

radioone(): This function is called when the page loads. It calls moviesearch() with the current value of the dropdown menu with the id selectinput.

radiotwo(): This function is likely intended to be called when the "series" radio button is selected. It calls seriessearch() with the current value of the dropdown menu with the id selectinput.

moviesearch(selectvalue): This function is an asynchronous function that sends a request to retrieve trending movies based on the selectvalue parameter (either "day" or "week"). It then populates the cards element with the received movie data.

seriessearch(selectvalue): Similar to moviesearch(), this function sends a request to retrieve trending TV series based on the selectvalue parameter. It populates the cards element with the received TV series data.

moviedeatils(id): This function is called when a movie poster is clicked. It stores the clicked movie's ID in the local storage under the key "movieid".

seriesdetails(id): This function is called when a TV series poster is clicked. It stores the clicked TV series' ID in the local storage under the key "seriesid".

getmoviedetails(): This function retrieves details for a specific movie using the stored movie ID. It sends a request to get movie details and populates the result element with the received data, including the movie's cast.

getseriesdetails(): Similar to getmoviedetails(), this function retrieves details for a specific TV series using the stored series ID. It populates the result element with the received data, including the series' cast.

findmovie(selectvalue): This function is called when a search is performed. It sends a request to search for movies or TV series based on the inputvalue and selectvalue parameters. It populates the cards element with the received search results.

findtv(selectvalue): Similar to findmovie(), this function searches for TV series based on the inputvalue and selectvalue parameters and populates the cards element.

input, cards, searchselect, selectvalue, moviedropdown, seriesdropdown: These are variable declarations using const to store references to various DOM elements. These elements are likely part of a search functionality in the webpage.

searchselect.addEventListener('change', (ele) => { ... }): This event listener listens for changes in the value of the searchselect element (a dropdown menu). When the value changes, it updates the selectvalue variable and attaches another event listener to either the moviedropdown or seriesdropdown based on the selected value.

movies(): This function is called immediately after the event listeners are set up. It seems to be responsible for initiating a search for movies or TV series based on the selected value.

async function findmovie(selectvalue) and async function findtv(selectvalue): These two functions perform similar tasks. They are called when a search is performed. They use the fetch API to make a request to search for movies or TV series based on the input value and selected category. The received data is then used to populate the cards element with search results.

function moviedeatils(id) and function seriesdetails(id): These functions are called when a movie or TV series poster is clicked, respectively. They store the clicked item's ID in the local storage.

localStorage.setItem('movieid', id) and localStorage.setItem('seriesid', id): These lines store the clicked movie or series ID in the local storage. This is likely done so that the details of the clicked item can be retrieved on a different page.

localStorage.getItem('movieid') and localStorage.getItem('seriesid'): These lines retrieve the stored movie or series ID from the local storage. This is used to retrieve details on a separate page.

localStorage.removeItem('movieid') and localStorage.removeItem('seriesid'): After the details of a movie or series have been retrieved, these lines remove the corresponding ID from local storage. This is likely done to clean up the storage after it's no longer needed.
