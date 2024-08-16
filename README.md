# URL Shortener Service

This is a simple URL shortener service built using Node.js. It allows you to shorten a valid URL and tracks the number of visits/clicks on the shortened URL.

## Features

- **URL Shortening:** Generates a short URL for a given valid URL.
- **Redirection:** Redirects users to the original URL when they visit the short URL.
- **Analytics:** Tracks and displays the total number of visits/clicks for each short URL.

## Routes

- **POST /url**
  - **Description:** Generates a new short URL.
  - **Request Body:** `{ "originalUrl": "<valid URL>" }`
  - **Response:** `{ "shortUrl": "example.com/random-id" }`
  
- **GET /:id**
  - **Description:** Redirects the user to the original URL.
  - **Params:** `id` - The unique identifier for the short URL.
  - **Response:** Redirection to the original URL.
  
- **GET /url/analytics/:id**
  - **Description:** Returns the total clicks/visits for the provided short URL.
  - **Params:** `id` - The unique identifier for the short URL.
  - **Response:** `{ "clicks": <number_of_clicks> }`


