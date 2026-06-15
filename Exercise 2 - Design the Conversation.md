Exercise 2 - Design the Conversation



1. **Pick the verb**
- show every game : GET

- add a new game: POST 

- replace game 5's details: PUT

- remove game 5: DELETE
  
  
  
  2. **Pick the status code**

- a game was found and returned; 2xx/200

- a new game was created; 2xx/201

- a game was deleted with nothing to send back; 2xx/204

-  the client asked for a game that doesn't exist; 4xx/404

- the client sent a broken request body; 4xx/400

-  the server's code crashed; 5xx/500
  
  

3. **Safe vs. idempotent**
   
   GET is a *SAFE method* only to read data and never changes it.
   
   *Idempotent method* is for methods that you will repeat many times
   
   such as GET,PUT,DELETE.
   
   POST is NOT SAFE, or Idempotent because it could create the same data multiple times
   
   
   
   4. **Read it raw**
   
   GET /api/games/3 HTTP/1.1      ***** //method *****
   Host: localhost:8080      ****** //**path********
   Accept: application/json    ***//Headers***
   
   
   
   HTTP/1.1 200 OK *** // Status line***
   Content-Type: application/json  ***//Headers***
   
   ***//the body which is JSON***
   
   "id": 3,
   "title": "Celeste",
   "releaseYear": 2018,
   "rating": 9.1
   
   


