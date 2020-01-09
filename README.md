# Data-science

- [Spotify Song Suggester API](#spotify-song-suggester-api)
  - [Usage](#usage)
    - [Suggestion of 30 songs based on one track_id given](#suggested-songs-based-on-a-song)
    - [Suggestion of 30 songs based on a list of favorited song track_ids](#suggested-songs-based-on-a-list-of-favorites)
    - [Testing](#testing-app)
  - [Deployment](#deployment)

## Spotify Song Suggester API

A simple back-end Flask API to suggest spotify songs in the Spotify Song Suggester app
based on a track_id chosen by the user or a list of favorite songs

---

## Usage

### Suggestion of 30 songs based on one track_id given

Endpoint to return a list of 30 suggestions based on one track_id given.

    /song/<song_id>

**Parameters:** None

- request:track_id

**Returns:** JSON array containing the full details of the top 30 suggestions for a track_id given.

Example:
` https://spotifyflask.herokuapp.com/song/6VjBxj5OhlHqL4h5qwo6gL`

Returns:

    `[{"index":37134,"artist_name":"Moby","track_id":"3UigcTkkcvBLnq6GVCjE3i","track_name":"Like a Motherless Child - Broken Places Remix","acousticness":0.00176,"danceability":0.573,"duration_ms":349747,"energy":0.858,"instrumentalness":0.301,"key":2,"liveness":0.208,"loudness":-6.335,"mode":1,"speechiness":0.0497,"tempo":101.984,"time_signature":4,"valence":0.241,"popularity":27,"genre":"electronic"}...`

---

### Suggestion of 30 songs based on a list of favorited song track_ids

Endpoint to return a list of 30 suggestions based on a list of favorited song track_ids.

    /favorites

**Parameters:**

- request: list of track_id's

**Returns:** JSON array containing the full details of the top 30 suggestions for a track_id given.

Example:



Returns:



### Testing

Flask API was tested in Postman.

---


The spotify song suggester API uses the Spotify Audio Features dataset, uploaded to Kaggle joined with webscraped genre.

A KNN model was pickled to be integrated into the Flask app. 
The app handles the requests, returning the appropriate JSON data.

## Deployment

Find the last version of the Flask API on:

[Suggestions example based on one song](https://spotifyflask.herokuapp.com/song/6VjBxj5OhlHqL4h5qwo6gL)

[Suggestions example based on a list of favorites]()

---
