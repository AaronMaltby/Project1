** TITLE ** SONG FINDER

The app will have a search button that can recieve input. The user will then type in a song title of any song they want that is stored in the API library. Then using the song title the API will retrieve the name of all the artists that have that song title. the problem that this app will solve is a quick and comprehensive solution for people who remember the name of the song but cannot remember the artist or would like to see if many artists have the same song titles.

here is the copy of the wireframe img

https://imgur.com/AShY69m

The API I am going to use is Deezer API https://rapidapi.com/deezerdevs/api/deezer-1 ar unirest = require("unirest");

var req = unirest("GET", "https://deezerdevs-deezer.p.rapidapi.com/search");

req.query({ "q": "eminem" });

req.headers({ "x-rapidapi-host": "deezerdevs-deezer.p.rapidapi.com", "x-rapidapi-key": "SIGN-UP-FOR-KEY" });

req.end(function (res) { if (res.error) throw new Error(res.error);

console.log(res.body);
});