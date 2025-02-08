# API Tests using Postman
> [!WARNING]
> Work in progress.

Hello,

The Trello API offers powerful functionality for developers to programmatically interact with boards, lists, and cards. As part of the QA process, I aim to develop a targeted set of tests to address key aspects of the API's functionality, security, and performance. While these tests are not exhaustive, they focus on critical areas to ensure the API behaves as expected under common and edge-case scenarios.

API Source: https://developer.atlassian.com/cloud/trello/guides/rest-api/api-introduction/#your-first-api-call \
API Documentation: https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-group-actions 

> [!IMPORTANT]
> A Trello account is needed in order to receive your unique API authentication Key and Token.

## Functionality Tests

### CRUD operations based on API documentation
:pushpin:	Few variables were defined in order to save time: apiKey, apiToken and baseUrl

***1. Get all boards request***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-group-boards \
Request method used: **GET** \
Parameters used: apiKey, apiToken 

![Screenshot of Get all boards request](Postman_GIT_Screenshots/GetAllBoards.jpg)

***2. Create a board***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-post \
Request method used: **POST** \
Parameters used: apiKey, apiToken, name

**Breakdown:** *In the following request we will create a new board named New Board Github having it's unique id.*

![Screenshot create a board](Postman_GIT_Screenshots/CreateNewBoard.jpg)

***3. Check created board***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-get \
Request method used: **GET** \
Parameters used: apiKey, apiToken, id (New Board Github generated id)

**Breakdown:** *In the following request we will verify if the new board (New Board Github) has been successfully created using it's generated id* 

![Screenshot verify created board](Postman_GIT_Screenshots/GetSingleBoard.jpg)

***4. Create a To Do list***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-post \
Request method used: **POST** \
Parameters used: apiKey, apiToken, idBoard, name

**Breakdown:** *In the following request we will create a To Do List inside the board.* 

![Screenshot create to do list](Postman_GIT_Screenshots/CreateToDoList.jpg)

***5. Update generated list***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-lists/#api-lists-id-put \
Request method used: **PUT** \
Parameters used: apiKey, apiToken, name, pos, id(list id)

**Breakdown:** *In the following request we want to update the name and pos of the "To Do" list. New name: WorkInProgress, New Pos: 8170* 

![Screenshot update to do list](Postman_GIT_Screenshots/UpdateToDoList.jpg)

***6. Delete New Board Github***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-delete \
Request method used: **Delete** \
Parameters used: apiKey, apiToken, id(board)

**Breakdown:** *In the following request we want to delete the board which we created in the first time.* 

![Screenshot delete created board](Postman_GIT_Screenshots/DeleteCreatedBoard.jpg)

***7. Verify deleted board***\
Documentation link: https://developer.atlassian.com/cloud/trello/rest/api-group-boards/#api-boards-id-get \
Request method used: **GET** \
Parameters used: apiKey, apiToken, id(board)

**Breakdown:** *In the following request we want to check if the deleted board was indeed deleted from the database* 

![Screenshot delete created board](Postman_GIT_Screenshots/DeletedBoardCheck.jpg)

## Script Tests 

***1. "Response body structure and data validation test"***\
Request method used: **GET** \
Parameters used: apiKey, apiToken, id (5901bedbfb1bfc2119b5cc58)

**Breakdown:** *The following script aims to verify few body response data* 

![Screenshot Body Response test](Postman_GIT_Screenshots/BodyResponseTests.jpg) \
:page_with_curl: Body response: [Here](Postman_GIT_Screenshots/BodyResponseGetSingleBoard.json)
