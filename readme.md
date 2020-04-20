<h1 align="center">
    <img alt="GoStack Bootcamp" src="https://res.cloudinary.com/marcelojrfarias/image/upload/v1587323057/gostack_gy3h7u.png" />
    <br>
    Challenge #1
    <br>
    Node.js Concepts
</h1>

<h4 align="center">
  An API to create, list, update, remove and like repositories.
</h4>
<p align="center">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/marcelojrfarias/gostack-nodejs_concepts.svg">
  
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/marcelojrfarias/gostack-nodejs_concepts.svg">
  
  <a href="https://www.codacy.com/manual/marcelojrfarias/gostack-nodejs_concepts?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=marcelojrfarias/gostack-nodejs_concepts&amp;utm_campaign=Badge_Grade">
    <img src="https://api.codacy.com/project/badge/Grade/2b9bd635f1644a4b8cb9ece8c8d2ac17"/>
  </a>
  
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/marcelojrfarias/gostack-nodejs_concepts.svg">
  <a href="https://github.com/marcelojrfarias/gostack-nodejs_concepts/commits/master">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/marcelojrfarias/gostack-nodejs_concepts.svg">
  </a>
  
  <a href="https://github.com/marcelojrfarias/gostack-nodejs_concepts/issues">
    <img alt="Repository issues" src="https://img.shields.io/github/issues/marcelojrfarias/gostack-nodejs_concepts.svg">
  </a>
  
  <img alt="GitHub" src="https://img.shields.io/github/license/marcelojrfarias/gostack-nodejs_concepts.svg"> 
</p>

<p align="center">
  <a href="#rocket-technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#gear-how-to-use">How To Use</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#link-routes">Routes</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-license">License</a>
</p>

## :rocket: Technologies

This project was developed at the [RocketSeat GoStack Bootcamp][gostack] with the following technologies:

- [NodeJS][nodejs]
- [Express][express]
- [Visual Studio Code][vscode]
- And some other packages...
  
## :gear: How To Use

To clone and run this application, you'll need [Git][git], [Node.js v10.16][nodejs] or higher + [Yarn v1.13][yarn] or higher installed on your computer. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/marcelojrfarias/gostack-nodejs_concepts

# Go into the repository
$ cd gostack-nodejs_concepts

# Install dependencies
$ yarn install

# Run the app
$ yarn start
```

## :link: Routes

<p align="center">
  <a href="#list-the-repositories">List</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#create-a-repository">Create</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#update-a-repository">Update</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#delete-a-repository">Delete</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#like-a-repository">Like</a>
</p>

<h1 align="center">
<a href="https://insomnia.rest/run/?label=NodejsConcepts&uri=https://raw.githubusercontent.com/marcelojrfarias/gostack-nodejs_concepts/master/insomnia.json" target="_blank"><img src="https://insomnia.rest/images/run.svg" alt="Run in Insomnia"></a>
</h1>

### List the repositories
#### Request
- **Method:**
  ```
  GET
  ```
- **Endpoint:**
  ```
  /repositories
  ```
- **Route Parameters:**
  ```
  None.
  ```
- **Query Parameter:**
  ```
  None.
  ```
- **Headers:**
  ```
  None.
  ```
- **Body:**
  ```
  None.
  ```
#### Response
##### Success
- **Code:**
  ```
  200
  ```
- **Content:**
  ```json
  [{
    "id": "87380836-6540-422e-9679-3d67115049d0",
    "title": "Backend with Node.js",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js"],
    "likes": 0
  },
  ]
  ```

### Create a repository
#### Request
- **Method:**
  ```
  GET
  ```
- **Endpoint:**
  ```
  /repositories
  ```
- **Route Parameters:**
  ```
  None.
  ```
- **Query Parameter:**
  ```
  None.
  ```
- **Headers:**
  ```
  None.
  ```
- **Body:**
  ```json
  {
    "title": "Backend with Node.js",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js"]
  }
  ```
#### Response
##### Success
- **Code:**
  ```
  200
  ```
- **Content:**
  ```json
  {
    "id": "87380836-6540-422e-9679-3d67115049d0",
    "title": "Backend with Node.js",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js"],
    "likes": 0
  }
  ```

### Update a repository
#### Request
- **Method:** 
  ```
  PUT
  ```
- **Endpoint:** 
  ```
  /repositories/:id
  ```
- **Route Parameters:**
  ```
  id: [string] (required)
  ```
- **Query Parameter:**
  ```
  None.
  ```
- **Headers:**
  ```
  None.
  ```
- **Body:**
  ```json
  {
    "title": "Backend with Node.js and Express",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js", "Express"]
  }
  ```
#### Response
##### Success
- **Code:** `200`
- **Content:**
  ```json
  {
    "id": "87380836-6540-422e-9679-3d67115049d0",
    "title": "Backend with Node.js and Express",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js", "Express"],
    "likes": 0
  }
  ```
##### Error
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Invalid project ID."
  }
  ```
OR
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Repository not found!"
  }
  ```
  
### Delete a repository
#### Request
- **Method:** 
  ```
  DELETE
  ```
- **Endpoint:** 
  ```
  /repositories/:id
  ```
- **Route Parameters:**
  ```
  id: [string] (required)
  ```
- **Query Parameter:**
  ```
  None.
  ```
- **Headers:**
  ```
  None.
  ```
- **Body:**
  ```
  None.
  ```
#### Response
##### Success
- **Code:** `204`
- **Content:**
  ```
  Empty.
  ```
##### Error
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Invalid project ID."
  }
  ```
OR
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Repository not found!"
  }
  ```
  
### Like a repository
#### Request
- **Method:** 
  ```
  POST
  ```
- **Endpoint:** 
  ```
  /repositories/:id/like
  ```
- **Route Parameters:**
  ```
  id: [string] (required)
  ```
- **Query Parameter:**
  ```
  None.
  ```
- **Headers:**
  ```
  None.
  ```
- **Body:**
  ```
  None.
  ```
#### Response
##### Success
- **Code:** `200`
- **Content:**
  ```json
  {
    "id": "87380836-6540-422e-9679-3d67115049d0",
    "title": "Backend with Node.js and Express",
    "url": "https://github.com/marcelojrfarias/gostack-nodejs_concepts",
    "techs": ["JavaScript", "Node.js", "Express"],
    "likes": 0
  }
  ```
##### Error
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Invalid project ID."
  }
  ```
OR
- **Code:** `400`
- **Content:**
  ```json
  {
    "error": "Repository not found!"
  }
  ```

## :memo: License
This project is under the MIT license. See the [LICENSE](https://github.com/marcelojrfarias/gostack-nodejs_concepts/blob/master/LICENSE) for more information.

---

Made with 💗 by Marcelo Farias 👋 [Get in touch!](https://www.linkedin.com/in/marcelojrfarias/)

[nodejs]: https://nodejs.org/
[gostack]: https://rocketseat.com.br/bootcamp
[express]: https://expressjs.com/
[git]: https://git-scm.com
[yarn]: https://yarnpkg.com/
[vscode]: https://code.visualstudio.com/
