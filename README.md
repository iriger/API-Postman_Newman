# API-Postman-Newman
This repository demonstrates API testing using Postman and Newman, showcasing best practices for testing REST APIs.
## Project Overview
This project consists of two parts:
1. A local API testing environment with a mock server
2. A CI/CD integration with automated test reports published to GitHub Pages
## Prerequisites
- Node.js (LTS version recommended)
- Postman application
### Part 1: Local API Testing
This part demonstrates testing of CRUD operations (POST, GET, PUT, DELETE) against a local mock API server.

Setup Instructions
1. Clone this repository
2. Install dependencies:   
     `npm i`
3. Start the local mock API server:

   `npm run tern-on-api`
4. Import the Postman collection:
  - Open Postman
  - Click "Import" button
  - Select the store.postman_collection.json file
  - Run the collection to execute all tests
### Part 2: Automated Testing with Newman
This part demonstrates continuous integration testing with automated reports.
#### Viewing Test Reports
The Newman test reports are automatically generated and published to GitHub Pages with each push to the main branch.
- View the latest test report: https://github.com/iriger/API-Postman_Newman
#### Running Tests Locally with Newman
You can also run the Newman tests locally:
1. Install Newman  (if not already installed):
2. npm install -g newman newman-reporter-htmlextra
3. Run the tests:
   
    `newman run petstore.collection.json -r htmlextra --reporter-htmlextra-export testResults/index.html`
5. Open the generated HTML report in your browser.
### CI/CD Integration
This project uses GitHub Actions to:
1. Run tests automatically on each push to the main branch
2. Generate HTML test reports using Newman
3. Publish reports to GitHub Pages for easy viewing
