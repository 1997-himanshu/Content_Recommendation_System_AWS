React.js + Flask Movie Recommendation System
Python Framework Frontend API

Overview 📋
The web app is built using React.js for the front-end and python's flask for the back-end.
It enable user to search and go through various details (like cast, genre, trailer, etc) 5000+ movies (all these details are fetched using an API by TMDB) .
Based on the searched movie users are recommended movie which are fetched for the python-flask backend that uses local dataset and content-based filtering algorithm for recommendation.
The web-app also allows user to get top movies filtered by genre (these are also fetched using an TMDB api) .
The web app is responsive and can be used on mobile devies.
Maintenance Website shields.io

Installation 📦
Clone or download this repository to your local machine.

Install all the libraries mentioned in the [requirements.txt]

$ pip install -r requirements.txt
Then run the flask server by

$ python app.py
Go to the movie-recommender-app directory and install the node modules and build the project.

$ cd movie-recommender-app
$ npm install
Go to the package.json file and change the proxy to your flask server local port which is most likely localhost:5000

Then build the project by

$ npm run build
To the local flask server to start the project

localhost :portNumber

If this doesn't work use

$ npm start
Architecture 📄
image

Algorithm For Recommendation
The Recommendations are made by computing similarity scores for movies using consine simarity. For each movie tags are created by combining various details like genre of the movie, title, top cast, director and then they are converted to vectors using which similarity matrix is formed. Then for any searched movie the movies with the largest similarity score with it are sorted and then recommended.

Cosine Similarity
image

References
TMDB's API : https://www.themoviedb.org/documentation/api
Cosine Similarity : https://www.machinelearningplus.com/nlp/cosine-similarity/
