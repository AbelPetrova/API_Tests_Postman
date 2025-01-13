# API Tests using Postman
Hello,

The Trello API offers powerful functionality for developers to programmatically interact with boards, lists, and cards. As part of the QA process, I aim to develop a targeted set of tests to address key aspects of the API's functionality, security, and performance. While these tests are not exhaustive, they focus on critical areas to ensure the API behaves as expected under common and edge-case scenarios.

API Source: https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/#your-first-api-call \
API Documentation: https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-group-actions 

> [!NOTE]
> A Trello account is needed in order to receive your unique API authentication Key and Token.

## Functionality Tests

### CRUD operations based on API documentation
:pushpin:	Few variables were defined in order to save time: apiKey, apiToken and baseUrl

***1. Get all boards request***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-group-boards \
Request method used: **GET** \
Parameters used: apiKey, apiToken 



