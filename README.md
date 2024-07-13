# Timestamp Microservice

This project is a Timestamp Microservice built with Node.js and Express. The application provides the current timestamp in both Unix and UTC formats, and it can also parse and return a timestamp for a given date string.

## Live Demo

You can see a live demo of the application here: [Timestamp Microservice](https://timestamp-microservice.freecodecamp.rocks)

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [License](#license)

## Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/hackim18/Backend-Timestamp-Microservice
   cd Backend-Timestamp-Microservice
   ```
2. **Install dependencies**:
   ```sh
   npm install
   ```
3. **Create a .env file** in the root of the project and add the following line:
   ```sh
   PORT=3000
   ```
4. **Start the server**:
   ```sh
   npm start
   The application will be running on http://localhost:3000.
   ```

## Usage

To use the Timestamp Microservice, you can make requests to the following endpoints:

## API Endpoints

1. **Root Endpoint**
   - **URL**: /
   - **Method**: GET
   - **Description**: Serves the homepage of the application.
   - **Example**: http://localhost:3000/
2. **Hello API**
   - **URL**: /api/hello
   - **Method**: GET
   - **Description**: Returns a greeting message in JSON format.
   - **Example**: http://localhost:3000/api/hello
   - **Response**:
     ```json
     {
       "greeting": "hello API"
     }
     ```
3. **Current Timestamp**
   - **URL**: /api
   - **Method**: GET
   - **Description**: Returns the current timestamp in Unix and UTC formats.
   - **Example**: http://localhost:3000/api
   - **Response**:
     ```json
     {
       "unix": 1609459200000,
       "utc": "Fri, 01 Jan 2021 00:00:00 GMT"
     }
     ```
4. **Timestamp for a Given Date**
   - **URL**: /api/:date
   - **Method**: GET
   - **Description**: Parses a date string and returns the timestamp in Unix and UTC formats. If the date string is invalid, it returns an error message.
   - **Example**:
     - Valid date string: http://localhost:3000/api/2021-01-01
     - Unix timestamp: http://localhost:3000/api/1609459200000
     - Invalid date string: http://localhost:3000/api/invalid-date
   - **Response**:
     - For a valid date string:
       ```json
       {
         "unix": 1609459200000,
         "utc": "Fri, 01 Jan 2021 00:00:00 GMT"
       }
       ```
     - For an invalid date string:
       ```json
       {
         "error": "Invalid Date"
       }
       ```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
