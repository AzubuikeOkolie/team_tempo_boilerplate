# [App Name] Integration Guide

# HNG Boilerplate API

This is the API documentation for the HNG Boilerplate project.

- [Hosted OpenApi Blueprint url](https://app.swaggerhub.com/apis-docs/GODHANDED0/hng-boilerplate_api/1.0.0)
- [OpenApi Api blueprint file](https://app.swaggerhub.com/apis/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Entity Relationship Diagram(ERD)](https://i.ibb.co/zrw8tTS/DB-Image.jpg)

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
- [OpenApi Api blueprint file](https://app.swaggerhub.com/apis/GODHANDED0/hng-boilerplate_api/1.0.0)
- [Entity Relationship Diagram(ERD)](https://i.ibb.co/zrw8tTS/DB-Image.jpg)
     
![ER Diagram](https://i.ibb.co/zrw8tTS/DB-Image.jpg)

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

[See OpenApi Scheme file for more Endpoints/Details](#openapi-specification)
  
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

  ### /v1/payments/
  #### POST
  - **Summary**: Process payments (Stripe, Flutterwave and LemonSqueezy) The initiatorId is used to bind between the UserId and OrganisationId. Also we are using one endpoint to make payments removinf the neeed to create seperate endpoints for different payments provider.
  - **Security**: BearerAuth
  - **Tags**: Payments
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - Type: `object`
          - Properties:
            - `reference`: `string`
            - `provider`: `string`
            - `metaData`: `string`
              - Example: 
                ```json
                {
                  "organisationId": "3432-fs334-4fduji-g56",
                  "productId": "suc231",
                  "productTye": "subscription",
                  "users": [
                    { "id": "5343-3ddnbd-0993435" },
                    { "id": "7343-3ddnbd-0993435" },
                    { "id": "67343-3ddnbd-0993435" },
                    { "id": "4343-3ddnbd-0993435" }
                  ]
                }
                ```
  - **Responses**:
    - `200`: Payment intent created
      - Content: 
        - `application/json`:
          - Schema:
            - Type: `object`
            - Properties:
              - `clientSecret`: `string`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `500`: Internal server error
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/superadmin/users
  #### GET
  - **Summary**: Get all users (Superadmin)
  - **Security**: BearerAuth
  - **Tags**: Superadmin Interface
  - **Responses**:
    - `200`: List of all users
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/User`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/superadmin/orgs
  #### GET
  - **Summary**: Get all organizations (Superadmin)
  - **Security**: BearerAuth
  - **Tags**: Superadmin Interface
  - **Responses**:
    - `200`: List of all organizations
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/Organisation`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/superadmin/payments
  #### GET
  - **Summary**: Get all payments (Superadmin)
  - **Security**: BearerAuth
  - **Tags**: Superadmin Interface
  - **Responses**:
    - `200`: List of all payments
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/Payment`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/superadmin/activity-log
  #### GET
  - **Summary**: Get activity log (Superadmin)
  - **Security**: BearerAuth
  - **Tags**: Superadmin Interface
  - **Responses**:
    - `200`: Activity log
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/ActivityLog`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/settings
  #### GET
  - **Summary**: Get application settings
  - **Security**: BearerAuth
  - **Tags**: Settings
  - **Responses**:
    - `200`: Application settings
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Settings`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
  #### PUT
  - **Summary**: Update application settings
  - **Security**: BearerAuth
  - **Tags**: Settings
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - `$ref`: `#/components/schemas/Settings`
  - **Responses**:
    - `200`: Settings updated
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Settings`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/landing/privacy-policy
  #### GET
  - **Summary**: Get privacy policy
  - **Tags**: Landing Pages
  - **Responses**:
    - `200`: Privacy policy
      - Content:
        - `text/html`:
          - Schema:
            - Type: `string`
            - Format: `html`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/landing/about-us
  #### GET
  - **Summary**: Get about us page
  - **Tags**: Landing Pages
  - **Responses**:
    - `200`: About us page
      - Content:
        - `text/html`:
          - Schema:
            - Type: `string`
            - Format: `html`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/contact-us
  #### POST
  - **Summary**: Submit a contact us form
  - **Tags**: Contact Us
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - Type: `object`
          - Properties:
            - `name`: `string`
            - `email`: `string`
              - Format: `email`
            - `message`: `string`
  - **Responses**:
    - `200`: Contact form submitted
      - Content:
        - `application/json`:
          - Schema:
            - Type: `object`
            - Properties:
              - `message`: `string`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/invite
  #### POST
  - **Summary**: Send an invite
  - **Security**: BearerAuth
  - **Tags**: Invite Flow
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - Type: `object`
          - Properties:
            - `email`: `string`
              - Format: `email`
  - **Responses**:
    - `200`: Invite sent successfully
      - Content:
        - `application/json`:
          - Schema:
            - Type: `object`
            - Properties:
              - `message`: `string`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/data-export
  #### POST
  - **Summary**: Export user data
  - **Security**: BearerAuth
  - **Tags**: Data Export
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - Type: `object`
          - Properties:
            - `email`: `string`
              - Format: `email`
  - **Responses**:
    - `200`: User data export initiated
      - Content:
        - `application/json`:
          - Schema:
            - Type: `object`
            - Properties:
              - `data`: `string`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/random-data
  #### GET
  - **Summary**: Get list of random data associated with user
  - **Security**: BearerAuth
  - **Tags**: Random Data
  - **Responses**:
    - `200`: List of random data
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/RandomData`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
  #### POST
  - **Summary**: Add random data
  - **Security**: BearerAuth
  - **Tags**: Random Data
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - `$ref`: `#/components/schemas/RandomData`
  - **Responses**:
    - `200`: Random data added
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/RandomData`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/random-data/{id}
  #### DELETE
  - **Summary**: Delete random data
  - **Security**: BearerAuth
  - **Tags**: Random Data
  - **Parameters**:
    - `id`: 
      - In: `path`
      - Required: true
      - Schema:
        - Type: `string`
  - **Responses**:
    - `204`: No content
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/chart-page
  #### GET
  - **Summary**: Retrieve chart data
  - **Security**: BearerAuth
  - **Tags**: Chart Page
  - **Responses**:
    - `200`: Chart data retrieved
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/ChartData`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/content-edit
  #### POST
  - **Summary**: Edit content
  - **Security**: BearerAuth
  - **Tags**: Content Edit Page
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - `$ref`: `#/components/schemas/ContentEdit`
  - **Responses**:
    - `200`: Content updated
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/ContentEdit`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/notifications
  #### GET
  - **Summary**: Get user notifications
  - **Security**: BearerAuth
  - **Tags**: Notifications
  - **Responses**:
    - `200`: List of notifications
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/Notification`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/blog
  #### GET
  - **Summary**: Get list of blog posts
  - **Security**: BearerAuth
  - **Tags**: Blog
  - **Responses**:
    - `200`: List of blog posts
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/BlogPost`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/invite-link
  #### POST
  - **Summary**: Generate invite link
  - **Security**: BearerAuth
  - **Tags**: Invite Link
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - Type: `object`
          - Properties:
            - `email`: `string`
              - Format: `email`
  - **Responses**:
    - `200`: Invite link generated
      - Content:
        - `application/json`:
          - Schema:
            - Type: `object`
            - Properties:
              - `inviteLink`: `string`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/language-region
  #### GET
  - **Summary**: Get available languages and regions
  - **Tags**: Language and Region
  - **Responses**:
    - `200`: List of languages and regions
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/LanguageRegion`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/email-templates
  #### GET
  - **Summary**: Get list of email templates
  - **Security**: BearerAuth
  - **Tags**: Email Template Management (HTML)
  - **Responses**:
    - `200`: List of email templates
      - Content:
        - `application/json`:
          - Schema:
            - Type: `array`
            - Items:
              - `$ref`: `#/components/schemas/EmailTemplate`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
  #### POST
  - **Summary**: Create email template
  - **Security**: BearerAuth
  - **Tags**: Email Template Management (HTML)
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - `$ref`: `#/components/schemas/EmailTemplate`
  - **Responses**:
    - `201`: Email template created
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/EmailTemplate`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  #### PUT
  - **Summary**: Update email template
  - **Security**: BearerAuth
  - **Tags**: Email Template Management (HTML)
  - **Request Body**:
    - Required: true
    - Content:
      - `application/json`:
        - Schema:
          - `$ref`: `#/components/schemas/EmailTemplate`
  - **Responses**:
    - `200`: Email template updated
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/EmailTemplate`
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

  ### /v1/email-templates/{id}
  #### DELETE
  - **Summary**: Delete email template
  - **Security**: BearerAuth
  - **Tags**: Email Template Management (HTML)
  - **Parameters**:
    - `id`: 
      - In: `path`
      - Required: true
      - Schema:
        - Type: `string`
  - **Responses**:
    - `204`: No content
    - `400`: Invalid request
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`
    - `401`: Unauthorized
      - Content:
        - `application/json`:
          - Schema:
            - `$ref`: `#/components/schemas/Error`

</details>


# Authors
- [@Godhanded]()
- [@OAK]()
- [@Pompey]()
- [Samba]()
- [~.]()