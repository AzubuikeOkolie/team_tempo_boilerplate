# [App Name] Integration Guide

# HNG Boilerplate API

This is the API documentation for the HNG Boilerplate project.
Here in includes Entity Realtionship Diagrams, Api Enpoint Specification, Resource Entity Descriptions and SetUp Information.

- [Hosted OpenApi Blueprint url](https://app.swaggerhub.com/apis-docs/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Hosted OpenApi Blueprint HTML](https://hng11openapi.netlify.app/)
- [OpenApi Api blueprint file](https://app.swaggerhub.com/apis/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Entity Relationship Diagram(ERD)](https://i.ibb.co/T4P0YmM/ERDiagram.jpg)
- [Entity Scheme file](https://drive.google.com/file/d/1758mgRWgUcXct-9Yippf-wIPG9dAZb7N/view?usp=sharing)

## Table Of Contents
- [Overview and Getting Started](#overview-and-getting-started)
  - [Folder Structure](#folder-structure)
  - [Getting Started](#getting-started)
  - [Setup Instructions](#setup-instructions)
- [Base Url](#base-url)
- [Api Specification/Design](#api-specificationdesign)
  - [Blueprint And Design Specification Links](#blueprint-and-design-specification-file-links)
    - [Entity Relationship Diagram(ERD)](#blueprint-and-design-specification-file-links)
  - [Data Structures](#datastructures)
    - [Error](#error)
    - [User](#user)
    - [BlogPost](#blogpost)
    - [Chart Data](#chartdata)
    - [Enum: Status](#enum-status)
    - [See OpenApi Specification]()
  - [Example Endpoints](#endpoints)
      - [See OpenApi Scheme file for more Endpoints/Details](#openapi-specification)
      - [Authentication Endpoints](#authentication-endpoint)
      - [User Management Endpoints](#user-management-endpoints)
      - [Organisation Management Endpoints](#organisation-management-endpoints)
      - [Messages Endpoints](#messages-endpoints)
  - [OpenAPI Specification](#openapi-specification)
- [Authors](#authors)

<hr>

## Overview and Getting Started  
<details id="overview-and-getting-started" >

  <summary>
  Click Here For Overview and Getting Started Details
  </summary>

  [Description]

  ## Folder Structure

  ```
  |--- .vscode
  |--- src
  |    |--- Hng.Application
  |    |--- Hng.Application.Test
  |    |--- Hng.Domain
  |    |--- Hng.Infrastructure
  |    |--- Hng.web
  |         |--- Controllers
  |         |--- Program.cs
  |         |--- .dockerignore
  |         |--- Dockerfile
  |         |--- appsettings.json
  |         |--- appsettings.Development.json
  |--- .gitignore
  |--- Hng.Csharp.Web.sln
  ```

  ## Getting started

  Ensure you have your computer setup correctly for development by installing the following

  - .Net 8 with C# 12.0
  - Visual studio 2019 or higher with ASP.Net web installation pack or
  - Visual studio code with .Net and C# dev extensions installed
  - Install .Net maui development pack for future uses

  ## Contribution Guide

  #### If you don't have git on your machine, [install it](https://docs.github.com/en/get-started/quickstart/set-up-git).

  ## Fork this repository

  Fork this repository by clicking on the fork button on the top of this page.
  This will create a copy of this repository in your account.

  ## Clone the repository

  <img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/clone.png" alt="clone this repository" />

  Now clone the forked repository to your machine. Go to your GitHub account, open the forked repository, click on the code button and then click the _copy to clipboard_ icon.

  Open a terminal and run the following git command:

  ```bash
  git clone "url you just copied"
  ```

  where "url you just copied" (without the quotation marks) is the url to this repository (your fork of this project). See the previous steps to obtain the url.

  <img align="right" width="300" src="https://firstcontributions.github.io/assets/Readme/copy-to-clipboard.png" alt="copy URL to clipboard" />

  For example:

  ```bash
  git clone git@github.com:this-is-you/hng_project.git
  ```

  where `this-is-you` is your GitHub username. Here you're copying the contents of the first-contributions repository on GitHub to your computer.

  ## Create a branch

  Change to the repository directory on your computer (if you are not already there):

  ```bash
  cd hng_project
  ```

  Now create a branch using the `git switch` command:

  ```bash
  git switch -c your-new-branch-name
  ```

  For example:

  ```bash
  git switch -c add-alonzo-church
  ```

  ### Make Changes

  Make your changes to the codebase. Ensure your code follows the project's coding standards and guidelines.

  ### Run Tests

  Run the existing tests to ensure your changes do not break anything. If you added new functionality, write corresponding tests and run them.

  ## commit those changes

  Now open `Contributors.md` file in a text editor, add your name to it. Don't add it at the beginning or end of the file. Put it anywhere in between. Now, save the file.

  <img align="right" width="450" src="https://firstcontributions.github.io/assets/Readme/git-status.png" alt="git status" />

  If you go to the project directory and execute the command `git status`, you'll see there are changes.

  Add those changes to the branch you just created using the `git add` command:

  ## Push changes to GitHub

  Push your changes using the command `git push`:

  ```bash
  git push -u origin your-branch-name
  ```

  replacing `your-branch-name` with the name of the branch you created earlier.

  <details>
  <summary> <strong>If you get any errors while pushing, click here:</strong> </summary>

  - ### Authentication Error
      <pre>remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
    remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
    fatal: Authentication failed for 'https://github.com/<your-username>/first-contributions.git/'</pre>
    Go to [GitHub's tutorial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) on generating and configuring an SSH key to your account.

  </details>

  ## Submit your changes for review into Staging

  If you go to your repository on GitHub, you'll see a `Compare & pull request` button. Click on that button.

  <img style="float: right;" src="https://firstcontributions.github.io/assets/Readme/compare-and-pull.png" alt="create a pull request" />

  Now submit the pull request.

  <img style="float: right;" src="https://firstcontributions.github.io/assets/Readme/submit-pull-request.png" alt="submit pull request" />

  Soon your changes will be merged into the staging branch of this project. You will get a notification email once the changes have been merged.

  ## Setup Instructions

  ### 1. Clone the Repository

  First, clone the repository to your local machine using Git.

  ```sh
  git clone https://github.com/your-username/[app-name].git
  cd [app-name]
  ```

  ### 2. Install Dependencies

  Opening the solution in Visual studio should automatically restore all your dependencies, you can ensure this by right clicking on the solution explorer and clicking `Restore dependencies`.

  If you are using Vscode with the required installations mentioned above, navigate to the project directory and install the required dependencies.

  ```sh
  dotnet restore
  ```

  ### 3. Run the Development Server

  Press `F5` on your keyboard to run the application in debug mode for both Visual studio and Vscode (You may need to open a .cs file to trigger this).

  Alternatively you can `cd` into `src/Hng.Web` project and run the command

  ```sh
  dotnet run
  ```

  ### 4. Verify the Setup

  Depending on the IDE/code editor, you should be greeted with the Swagger documentation page else navigate to `/swagger` to view the documentation
</details>



## Base URL

- Production: `https://api.hngboilerplate.com/`
- Staging: `https://api.staging.hngboilerplate.com/`

## Api Specification/Design
### Blueprint and Design specification file Links
- [Hosted OpenApi Blueprint url](https://app.swaggerhub.com/apis-docs/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Hosted OpenApi Blueprint HTML](https://hng11openapi.netlify.app/)
- [OpenApi Api blueprint file](https://app.swaggerhub.com/apis/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Entity Relationship Diagram(ERD)](https://i.ibb.co/T4P0YmM/ERDiagram.jpg)
- [Entity Specification File](https://drive.google.com/file/d/1758mgRWgUcXct-9Yippf-wIPG9dAZb7N/view?usp=sharing)
     
![ER Diagram](https://i.ibb.co/T4P0YmM/ERDiagram.jpg)

### DataStructures
- #### Error
  - Type: `object`
  - Properties:
    - `code`: `integer`
    - `message`: `string`

- #### User
  - Type: `object`
  - Properties:
    - `id`: `string`
    - `username`: `string`
    - `email`: `string`
    - `isActive`: `boolean`


- #### ChartData
  - Type: `object`
  - Properties:
    - `id`: `string`
    - `value`: `number`

- #### BlogPost
  - Type: `object`
  - Properties:
    - `id`: `string`
    - `title`: `string`
    - `content`: `string`

- #### Enum: Status
  | Name     | Value |
  |----------|-------|
  | Active   | 1     |
  | Disabled | 2     |
  | Delete   | 3     |

[See Entity Scheme file for more Entities/Details]()
  
<br>

### Endpoints
<hr>

### Authentication Endpoint

#### User Registration

**Endpoint:** `/auth/register`  
**Method:** `POST`  
**Description:** Allows a new user to register.

#### Social Login + Magic Link

**Endpoint:** `/auth/social-login`  
**Method:** `POST`  
**Description:** Allows a user to log in using third-party OAuth providers like Google or Microsoft.

...
[See OpenApi Scheme file for more Endpoints/Details](#openapi-specification)

### User Management Endpoints

#### Get User Information

**Endpoint:** `/v1/users`  
**Method:** `GET`  
**Description:** Retrieves information about the currently logged-in user.

#### Retrieve Notifications

**Endpoint:** `/v1/users/notifications`  
**Method:** `GET`  
**Description:** Retrieves notifications for the currently logged-in user.

...
[See OpenApi Scheme file for more Endpoints/Details](https://drive.google.com/file/d/1JXg43RxSbjt6gW8wxkvx2CZfvO_EYuAb/view?usp=sharing)

### Organisation Management Endpoints

#### Create a New Organisation

**Endpoint:** `/v1/organisations`  
**Method:** `POST`  
**Description:** Creates a new organisation.

#### Get User by ID in Organisation

**Endpoint:** `/v1/organisations/users/{userId}`  
**Method:** `GET`  
**Description:** Retrieves details of a user in the organisation by their ID.

...
[See OpenApi Scheme file for more Endpoints/Details](#openapi-specification)

### Messages Endpoints

#### Start a New Conversation

**Endpoint:** `/v1/messages`  
**Method:** `POST`  
**Description:** Starts a new conversation.

...
[See OpenApi Scheme file for more Endpoints/Details](#openapi-specification)

# OpenAPI Specification
- [See Hosted Swagger Page of OpenApi Specification]()
<details>
  <summary> Click to View Sepcification </summary>


## Info
- Version: 3.0.1
- Title: HNG Boilerplate API
- Description: API for the HNG boilerplate project
- Version: 1.0.0

## Servers
- URL: https://api.hngboilerplate.com/
  Description: Main (production) server
- URL: https://api.staging.hngboilerplate.com/
  Description: Staging server

## Components
### Security Schemes
- BearerAuth:
  - Type: http
  - Scheme: bearer

### Schemas
- BaseEntity:
  - Type: object
  - Properties:
    - createdOn:
      - Type: string
      - Format: date-time
    - createdBy:
      - Type: string
    - modifiedOn:
      - Type: string
      - Format: date-time
    - modifiedBy:
      - Type: string
    - status:
      - Type: integer

- Page:
  - Type: object
  - Properties:
    - name:
      - Type: string
      - Example: "page name"
    - content:
      - Type: string
      - Example: |
          <html>
            <head>
              <title>Sample Page</title>
            </head>
            <body>
              <h1>Welcome to the Sample Page</h1>
              <p>This is a simple HTML page example.</p>
            </body>
          </html>

- User:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - name:
      - Type: string
    - email:
      - Type: string
      - Format: email
    - organisationId:
      - Type: string
      - Format: uuid
    - role:
      - Type: string
  - allOf:
    - $ref: '#/components/schemas/BaseEntity'

- InviteFlow:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - email:
      - Type: string
      - Format: email
  - allOf:
    - $ref: '#/components/schemas/BaseEntity'

- Organisation:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - name:
      - Type: string
    - createdAt:
      - Type: string
      - Format: date-time
    - createdby:
      - Type: string
    - modifiedby:
      - Type: string
    - updatedAt:
      - Type: string
      - Format: date-time

- Error:
  - Type: object
  - Properties:
    - code:
      - Type: integer
    - message:
      - Type: string

- LoginRequest:
  - Type: object
  - Properties:
    - email:
      - Type: string
      - Format: email
    - password:
      - Type: string

- LoginResponse:
  - Type: object
  - Properties:
    - token:
      - Type: string
    - user:
      - $ref: '#/components/schemas/User'

- RegisterRequest:
  - Type: object
  - Properties:
    - firstname:
      - Type: string
    - lastname:
      - Type: string
    - email:
      - Type: string
      - Format: email
    - password:
      - Type: string
    - createdAt:
      - Type: string
      - Format: date-time
    - updatedAt:
      - Type: string
      - Format: date-time

- RegisterResponse:
  - Type: object
  - Properties:
    - token:
      - Type: string
    - user:
      - $ref: '#/components/schemas/User'

- Payment:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - reference:
      - Type: string
    - amount:
      - Type: string
    - status:
      - Type: string
    - createdOn:
      - Type: string
      - Format: date-time
    - createdBy:
      - Type: string
    - provider:
      - Type: integer
    - metaData:
      - Type: string

- ActivityLog:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - userId:
      - Type: string
      - Format: uuid
    - action:
      - Type: string
    - timestamp:
      - Type: string
      - Format: date-time
    - description:
      - Type: string
    - organisationId:
      - Type: string
      - Format: uuid
    - activity:
      - Type: string
      - Enum:
        - automation
        - user
        - organisation
      - Example: automation

- Settings:
  - Type: object
  - Properties:
    - siteName:
      - Type: string
    - siteUrl:
      - Type: string
    - adminEmail:
      - Type: string
      - Format: email
    - isDarkMode:
      - Type: boolean
    - isprofilevissible:
      - Type: boolean

- UserProfile:
  - Type: object
  - Properties:
    - firstname:
      - Type: string
    - lastname:
      - Type: string
    - avatarUrl:
      - Type: string

- RandomData:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - name:
      - Type: string
    - description::
      - Type: string     

- OtherData:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - name:
      - Type: string
    - description:
      - Type: string

- ConversationMessage:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - message:
      - Type: string
    - createdBy:
      - Type: string
    - createdOn:
      - Type: string
      - Format: date-time
    - isRead:
      - Type: boolean

- Conversation:
  - Type: object
  - Properties:
    - id:
      - Type: string
      - Format: uuid
    - title:
      - Type: string
      - Example: "Channel-abc"
    - createdBy:
      - Type: string
    - createdOn:
      - Type: string
      - Format: date-time

## Paths

### /auth/login
- POST
  - Summary: User login
  - Tags: Authentication
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - $ref: '#/components/schemas/LoginRequest'
  - Responses:
    - '200':
      - Description: Successful login
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/LoginResponse'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /auth/register
- POST
  - Summary: User registration
  - Tags: Authentication
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - $ref: '#/components/schemas/RegisterRequest'
  - Responses:
    - '201':
      - Description: Successful registration
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/RegisterResponse'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /auth/social-login
- POST
  - Summary: Social login + magic link (third party oauth like Google, Microsoft etc)
  - Tags: Authentication
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - token:
              - Type: string
  - Responses:
    - '200':
      - Description: Successful social login
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/LoginResponse'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /auth/change-password
- POST
  - Summary: Change password
  - Tags: Authentication
  - Security:
    - BearerAuth: []
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - currentPassword:
              - Type: string
            - newPassword:
              - Type: string
  - Responses:
    - '200':
      - Description: Password changed successfully
      - Content:
        - application/json:
          - Schema:
            - Type: object
            - Properties:
              - message:
                - Type: string
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/users
- GET
  - Summary: Get the currently loggedin users information
  - Tags: User Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: User details
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/User'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: User not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

- PUT
  - Summary: Update the currently loggedin users information
  - Tags: User Management
  - Security:
    - BearerAuth: []
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - firstname:
              - Type: string
            - lastname:
              - Type: string
            - email:
              - Type: string
              - Format: email
  - Responses:
    - '200':
      - Description: User updated
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/User'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: User not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

- DELETE
  - Summary: Delete the currently loggedin users information
  - Tags: User Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '204':
      - Description: User deleted
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: User not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/users/invite-link
- GET
  - Summary: Get invite link
  - Tags: User Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: Successful response with invite link.
      - Content:
        - application/json:
          - Schema:
            - Type: object
            - Properties:
              - inviteLink:
                - Type: string

### /v1/users/notifications
- GET
  - Summary: Retrieve notifications
  - Tags: User Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: Successful response with notifications.
      - Content:
        - application/json:
          - Schema:
            - Type: array
            - Items:
              - Type: object
              - Properties:
                - id:
                  - Type: string
                  - Format: uuid
                - message:
                  - Type: string
                - status:
                  - Type: string
                  - Example: unread
                - createdOn:
                  - Type: string
                  - Format: date-time

### /v1/organisations
- GET
  - Summary: Get all organisations
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: List of organisations
      - Content:
        - application/json:
          - Schema:
            - Type: array
            - Items:
              - $ref: '#/components/schemas/Organisation'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

- POST
  - Summary: Create a new organisation
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - name:
              - Type: string
  - Responses:
    - '201':
      - Description: Organisation created
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Organisation'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/organisations/{organisationId}
- GET
  - Summary: Get organisation by ID
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Parameters:
    - In: path
      Name: organisationId
      Required: true
      Schema:
        Type: string
        Format: uuid
  - Responses:
    - '200':
      - Description: Organisation details
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Organisation'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: Organisation not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

- PUT
  - Summary: Update organisation by ID
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Parameters:
    - In: path
      Name: organisationId
      Required: true
      Schema:
        Type: string
        Format: uuid
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - name:
              - Type: string
  - Responses:
    - '200':
      - Description: Organisation details
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Organisation'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: Organisation not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/organisations/users
- GET
  - Summary: Get all users in the organisation
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: List of users
      - Content:
        - application/json:
          - Schema:
            - Type: array
            - Items:
              - $ref: '#/components/schemas/User'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/organisations/users/{userId}
- GET
  - Summary: Get user by ID
  - Tags: Organisation Management
  - Security:
    - BearerAuth: []
  - Parameters:
    - In: path
      Name: userId
      Required: true
      Schema:
        Type: string
        Format: uuid
  - Responses:
    - '200':
      - Description: User details
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/User'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '401':
      - Description: Unauthorized
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '404':
      - Description: User not found
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

### /v1/messages
- POST
  - Summary: Start a new conversation
  - Tags: Messages
  - Security:
    - BearerAuth: []
  - Request Body:
    - Required: true
    - Content:
      - application/json:
        - Schema:
          - Type: object
          - Properties:
            - conversationType:
              - Type: string
              - Example: Channel, Private
            - to:
              - Type: string
              - Format: uuid
            - message:
              - Type: string
  - Responses:
    - '200':
      - Description: Conversation sent successfully
      - Content:
        - application/json:
          - Schema:
            - allOf:
              - $ref: '#/components/schemas/ConversationMessage'
    - '400':
      - Description: Invalid request
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'
    - '500':
      - Description: Internal server error
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

- GET
  - Summary: Get conversations
  - Tags: Messages
  - Security:
    - BearerAuth: []
  - Responses:
    - '200':
      - Description: List of user conversations
      - Content:
        - application/json:
          - Schema:
            - Type: array
            - Items:
              - allOf:
                - $ref: '#/components/schemas/Conversation'
    - '500':
      - Description: Internal server error
      - Content:
        - application/json:
          - Schema:
            - $ref: '#/components/schemas/Error'

## /v1/messages/{conversationId}

### GET
- **Summary:** Get all the messages for a conversation
- **Security:** BearerAuth
- **Tags:** Messages
- **Parameters:**
  - **Path Parameters:**
    - `conversationId` (required, string, format: uuid)
- **Responses:**
  - `200`:
    - **Description:** List of conversation messages
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/ConversationMessage"
        }
      }
      ```
  - `500`:
    - **Description:** Internal server error
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/payments/

### POST
- **Summary:** Process payments (Stripe, Flutterwave and LemonSqueezy)
- **Security:** BearerAuth
- **Tags:** Payments
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "type": "object",
      "properties": {
        "reference": {
          "type": "string"
        },
        "provider": {
          "type": "string"
        },
        "metaData": {
          "type": "string",
          "example": {
            "organisationId": "3432-fs334-4fduji-g56",
            "productId": "suc231",
            "productTye": "subscription",
            "users": [
              {
                "id": "5343-3ddnbd-0993435"
              },
              {
                "id": "7343-3ddnbd-0993435"
              },
              {
                "id": "67343-3ddnbd-0993435"
              },
              {
                "id": "4343-3ddnbd-0993435"
              }
            ]
          }
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Payment intent created
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "clientSecret": {
            "type": "string"
          }
        }
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `500`:
    - **Description:** Internal server error
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/superadmin/users

### GET
- **Summary:** Get all users (Superadmin)
- **Security:** BearerAuth
- **Tags:** Superadmin Interface
- **Responses:**
  - `200`:
    - **Description:** List of all users
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/User"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/superadmin/orgs

### GET
- **Summary:** Get all organizations (Superadmin)
- **Security:** BearerAuth
- **Tags:** Superadmin Interface
- **Responses:**
  - `200`:
    - **Description:** List of all organizations
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/Organisation"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/superadmin/payments

### GET
- **Summary:** Get all payments (Superadmin)
- **Security:** BearerAuth
- **Tags:** Superadmin Interface
- **Responses:**
  - `200`:
    - **Description:** List of all payments
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/Payment"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/superadmin/activity-log

### GET
- **Summary:** Get activity log (Superadmin)
- **Security:** BearerAuth
- **Tags:** Superadmin Interface
- **Responses:**
  - `200`:
    - **Description:** Activity log
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/ActivityLog"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/settings

### GET
- **Summary:** Get application settings
- **Security:** BearerAuth
- **Tags:** Settings
- **Responses:**
  - `200`:
    - **Description:** Application settings
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Settings"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

### PUT
- **Summary:** Update application settings
- **Security:** BearerAuth
- **Tags:** Settings
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "$ref": "#/components/schemas/Settings"
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Settings updated
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Settings"
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/landing/privacy-policy

### POST
- **Summary:** Create privacy policy
- **Tags:** Landing Pages
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "$ref": "#/components/schemas/Page"
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Privacy policy
    - **Content:** text/html
      ```html
      {
        "type": "string",
        "format": "html"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/landing/about-us

### POST
- **Summary:** Create about us page
- **Tags:** Landing Pages
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "$ref": "#/components/schemas/Page"
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** About us page
    - **Content:** text/html
      ```html
      {
        "type": "string",
        "format": "html"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/contact-us

### POST
- **Summary:** Create contact us information
- **Tags:** Contact us
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "$ref": "#/components/schemas/Page"
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Contact form submitted
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "message": {
            "type": "string"
          }
        }
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/invite

### POST
- **Summary:** Send an invite
- **Security:** BearerAuth
- **Tags:** Invite Flow
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "type": "object",
      "properties": {
        "email": {
          "type": "string",
          "format": "email"
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Invite sent successfully
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "message": {
            "type": "string"
          }
        }
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/data-export

### POST
- **Summary:** Export user data
- **Security:** BearerAuth
- **Tags:** Data Export
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "type": "object",
      "properties": {
        "email": {
          "type": "string",
          "format": "email"
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** User data export initiated
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "data": {
            "type": "string"
          }
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/random-data

### GET
- **Summary:** Get list of random data associated with user
- **Security:** BearerAuth
- **Tags:** Random Data
- **Responses:**
  - `200`:
    - **Description:** List of random data
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/RandomData"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/random-data/{dataId}

### GET
- **Summary:** Get single random data by ID
- **Security:** BearerAuth
- **Tags:** Random Data
- **Parameters:**
  - **Path Parameters:**
    - `dataId` (required, string, format: uuid)
- **Responses:**
  - `200`:
    - **Description:** Single random data details
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/RandomData"
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `404`:
    - **Description:** Data not found
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/other-data

### GET
- **Summary:** Get list of other data with search and sorting
- **Security:** BearerAuth
- **Tags:** Random Data
- **Parameters:**
  - **Query Parameters:**
    - `search` (optional, string)
    - `sortBy` (optional, string)
    - `sortOrder` (optional, string, enum: [asc, desc])
- **Responses:**
  - `200`:
    - **Description:** List of other data with search and sorting
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "$ref": "#/components/schemas/OtherData"
        }
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

## /v1/chart

### GET
- **Summary:** Retrieve chart data
- **Security:** BearerAuth
- **Tags:** Chart
- **Description:** Endpoint to fetch data for displaying charts.
- **Responses:**
  - `200`:
    - **Description:** Successful response with chart data.
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "chartName": {
            "type": "string"
          },
          "chartDescription": {
            "type": "string"
          },
          "chartData": {
            "type": "array",
            "items": {
              "type": "object",
              "properties": {
                "label": {
                  "type": "string"
                },
                "value": {
                  "type": "number",
                  "format": "float"
                }
              }
            }
          }
        }
      }
      ```

## /v1/content/{id}

### PUT
- **Summary:** Update content by ID
- **Security:** BearerAuth
- **Tags:** Content
- **Description:** Endpoint to update content based on its ID.
- **Parameters:**
  - **Path Parameters:**
    - `id` (required, string)
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "type": "object",
      "properties": {
        "content": {
          "type": "string"
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Content updated successfully.

## /v1/blog

### POST
- **Summary:** Create blog posts
- **Security:** BearerAuth
- **Tags:** Blog
- **Description:** Endpoint to create blog posts.
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "type": "object",
      "properties": {
        "title": {
          "type": "string"
        },
        "content": {
          "type": "string"
        },
        "tag": {
          "type": "string",
          "example": "tech, info, crypto"
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Blog post successfully created.
    - **Content:** application/json
      ```json
      {
        "type": "object",
        "properties": {
          "id": {
            "type": "string",
            "format": "uuid"
          },
          "title": {
            "type": "string"
          },
          "content": {
            "type": "string"
          },
          "author": {
            "type": "string"
          },
          "tags": {
            "type": "array",
            "items": {
              "type": "string",
              "example": "tech, info, crypto"
            }
          },
          "createdOn": {
            "type": "string",
            "format": "date-time"
          }
        }
      }
      ```

### GET
- **Summary:** Retrieve blog posts
- **Security:** BearerAuth
- **Tags:** Blog
- **Description:** Endpoint to fetch blog posts.
- **Responses:**
  - `200`:
    - **Description:** Successful response with blog posts.
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "type": "object",
          "properties": {
            "id": {
              "type": "string",
              "format": "uuid"
            },
            "title": {
              "type": "string"
            },
            "content": {
              "type": "string"
            },
            "author": {
              "type": "string"
            },
            "tags": {
              "type": "array",
              "items": {
                "type": "string",
                "example": "tech, info, crypto"
              }
            },
            "createdOn": {
              "type": "string",
              "format": "date-time"
            }
          }
        }
      }
      ```

## /v1/language-region

### GET
- **Summary:** Retrieve language and region settings
- **Security:** BearerAuth
- **Tags:** Language Region
- **Description:** Endpoint to fetch language and region settings.
- **Responses:**
  - `200`:
    - **Description:** Successful response with language and region settings.
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "properties": {
            "language": {
              "type": "string"
            },
            "region": {
              "type": "string"
            }
          }
        }
      }
      ```

## /v1/email-templates

### GET
- **Summary:** Retrieve email templates
- **Security:** BearerAuth
- **Tags:** Email Templates
- **Description:** Endpoint to fetch email templates in HTML format.
- **Responses:**
  - `200`:
    - **Description:** Successful response with email templates.
    - **Content:** application/json
      ```json
      {
        "type": "array",
        "items": {
          "properties": {
            "id": {
              "type": "string",
              "format": "uuid"
            },
            "content": {
              "type": "string",
              "example": "<html><head><title>Email Template</title></head><body><h1>Welcome!</h1><p>This is an email template.</p></body></html>"
            },
            "createdOn": {
              "type": "string",
              "format": "date-time"
            },
            "createdBy": {
              "type": "string"
            },
            "modifiedOn": {
              "type": "string",
              "format": "date-time"
            },
            "modifiedby": {
              "type": "string"
            }
          }
        }
      }
      ```

## /v1/email-templates/{templateId}

### PUT
- **Summary:** Update email template content
- **Security:** BearerAuth
- **Tags:** Email Templates
- **Description:** Endpoint to update email templates in HTML format.
- **Parameters:**
  - **Path Parameters:**
    - `templateId` (required, string)
- **Request Body:**
  - **Content:** application/json
    ```json
    {
      "properties": {
        "content": {
          "type": "string"
        }
      }
    }
    ```
- **Responses:**
  - `200`:
    - **Description:** Successful login
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/LoginResponse"
      }
      ```
  - `400`:
    - **Description:** Invalid request
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```
  - `401`:
    - **Description:** Unauthorized
    - **Content:** application/json
      ```json
      {
        "$ref": "#/components/schemas/Error"
      }
      ```

</details>


# Authors
- [@Godhanded]()
- [@OAK]()
- [@Pompey]()
- [Samba]()
- [~.]()