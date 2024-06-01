# API Testing a real web application via Postman - Spotify API Testing using Postman
This repository contains resources related to the "API Testing a real web application via Postman" guided project. Here, you'll find the Postman collections and environments created.

- [Introduction](#introduction)
- [Learning Milestones](#learning-milestones)
- [Technologies Used](technologies-used)
- [Add-ons](#add-ons)
- [Directory Structure](#directory-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributions](#contributions)
- [Disclaimer](#disclaimer)

## Introduction
The "[API Testing a real web application via Postman](https://www.coursera.org/projects/api-testing-a-real-application-via-postman)" allowed me to practice writing scripts to test APIs using Postman, how to test CRUD (Create, Read, Update, and Delete) operations with HTTP methods like GET, POST, PUT and DELETE, understanding OAuth 2.0 flow, getting grant access, getting Access Token, understanding JSON request and response, and adding assertions to the API response.

## Learning Milestones
- Sending a GET request
- Understanding OAuth 2.0 flow
- Getting grant access
- Getting Access Token
- Using Refresh Token
- Adding user-defined variables
- Sending POST, PUT and DELETE requests
- Understanding the JSON response and Adding assertions for validation
- Generating reports using Newman


## Technologies Used
- [Spotify Web API](https://developer.spotify.com/documentation/web-api)
- [Postman](https://www.postman.com)
- [newman](https://www.npmjs.com/package/newman)
- [newman-reporter-htmlextra](https://www.npmjs.com/package/newman-reporter-htmlextra)

## Add-ons
In addition to the functionalities covered in the guided project, I've made the following custom additions to the collections:
- Transitioned from manually executing the OAuth2 flow to obtain tokens to embedding the OAuth2 flow within the collection's authorization tab, thereby streamlining the authentication process.
- Added multiple assertions to evaluate the integrity of the JSON response and enhance the test results.
- Implemented a 60-second wait before verifying the playlist update to prevent false positives caused by delayed reflection of modifications.
- Extracted the IDs and URIs embedded within the JSON response, which serves as input for the subsequent test cases.
- Created environment variables for flexible test configuration.
- Enhanced Test Suite Scope:
    - Expanded test coverage to include functionalities beyond user ID retrieval, playlist creation, and playlist information updates.
    - Integrated tests for the search functionality, including attributes such as limits and regions.
    - Implemented tests for playlist manipulation, including item addition and deletion.
- Generated an HTML report using Newman for a more user-friendly and visually appealing way to showcase the test results.

## Directory Structure
- `newman/`: The directory where HTML Reports are located.
  - `HTML_Report.html`:  This HTML file provides a detailed overview of the test execution results.
- `SpotifyAppTest.postman_collection.json`: This file contains a collection of API requests, organized and grouped for testing the JSON Server API. It is used to perform various API tests.
- `Spotify_Test.postman_environment.json`: This file stores the environment-specific variables and configurations used for the Spotify testing environment. This is the environment selected to test the API using Newman.

## Getting Started
1. Install Postman: [https://www.postman.com/downloads](https://www.postman.com/downloads/)
2. Import Collections:
    - Download the entire repository or specific files.
    - In Postman, open `"File"` -> `"Import"` -> `"Select Files"` and choose the downloaded files.
3. Configure Environments:
    - Choose the appropriate environment file for your testing environment (e.g., "Spotify_Test.postman_environment.json").
    - Go to `"File"` -> `"Import"` -> `"Select Files"` and select the chosen file.
4. Follow Spotify API Getting Started instructions:
    - Refer to [https://developer.spotify.com/documentation/web-api](https://developer.spotify.com/documentation/web-api) to create an application within your Spotify Developer Dashboard.
    - Ensure that the `Callback URL` and the `State` values in the collection match those specified in your application.
    - For automatic token refreshing, ensure to activate the `"Auto-refresh Token"` toggle.
5. Set up environment variables:
    - Copy your Client ID to the `"Client_ID"` variable within the `"Spotify_Test"` environment.
    - Copy your Client Secret to the `"Client_Secret"` variable within the `"Spotify_Test"` environment.
6. Run Tests:
    - Within the collection, you can run individual requests or the entire collection.
    - When running the tests using `"newman"` it is important to activate the `"Share Token"` toggle to ensure a successful execution.


## Usage
You can go ahead and explore my collections and environments. Feel free to use these collections as reference, study materials, or review materials to enhance your understanding of Postman.

## Contributions
Contributions to this repository are welcome. If you have alternative code implementations, suggestions for improvements please consider submitting a pull request. If you encounter any issues with my implementation or have additional insights to share, please open an issue.

## Disclaimer
> This is not the official implementation.
