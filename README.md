

## GraphQL Schema Explorer
Locate src/App.js line:15 to change the host


The server supports cookies and token auth

To update the token:
Get the token from the server and replace in `src/App.js`
```
mutation{
  signInUser(input: { credentials: { email: "admin@app.io", password: "admin" } }) {
      token
    }
  }

```

replace it at:

```javascript
let auth = {
	heroku:{
		url: "https://myapi.herokuapp.com/graphql",
		token: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJmb28iOiJiYXIiLCJleHAiOjE1ODc3MzA3MDd9.Q5YZtB2pGK9kBbDbiwgjuvwAOOULsWZ7BKz90cl6cok'
	},
	localhost:{
		url: "http://127.0.0.1:3030/graphql",
		token: 'Bearer eyJhbGciOiJIUzI1NiJ9.eyJmb28iOiJiYXIiLCJleHAiOjE1ODc3MzA3MDd9.Q5YZtB2pGK9kBbDbiwgjuvwAOOULsWZ7BKz90cl6cok'	
	}}
```



## Setup

Install dependencies:

```
npm install
# or
yarn install
```

Start the server:

```
npm run start
# or
yarn start
```

Your browser will automatically open to http://localhost:3000 with the explorer open.
