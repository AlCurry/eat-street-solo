# eat-street-solo

eat-street-style is a cleaner version of this repo, but with slightly different look - darker theme.

restLogic.js and api-routes.js are a bit of a mess here - left that way for now - due to issues deploying on heroku
it turns out the npm package reverse-geocode, being used on the server side to translate a longitude and latitude to a zip code was
failing on heroku, though it worked fine locally

Heroku message was internal server error, flagging the line of the route -
jquery-3.3.1.min.js:2 GET https://aqueous-chamber-68199.herokuapp.com/api/restlist/40.6930607/-73.9938488 500 (Internal Server Error) 
inconveniently with a not too consistent call stack dump beneath the error

It took a few tries to unearth the problem (an aqueous chamber helped doh) - at some point hope to try another reverse geocode utility,
but content for the moment to know the cause, at least vaguely - curious to know exactly why that package has issues on heroku, but 
logs there and my experience with heroku's environment keep the precise errors a bit of a mystery.

Stand-alone version of eatstreet app using their npm package - part of GWU full stack web dev program.

To be integrated in to our project "Netflix&Chill" - this piece allows one to get a list of food delivery option available locally.

For now, not optimally, the npm/api key is still in the code, rather than a separate .env location.

Note also uses the reverse-lookup package - given latitude & longitude on the client side, return zip code on the server for 
restaurant lookup.

'npm install' must be run to install packages before executing
