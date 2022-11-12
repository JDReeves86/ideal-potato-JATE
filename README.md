# 19 Progressive Web Applications (PWA): Text Editor


## ideal-potato- Text Editor

---

### Contents 

---

1. Objectives
2. About
4. Links
5. Assignment details & grading rubric (*ignore me*)

<br>
<br>

### Objectives ###

---

<br>

1. WHEN the application is opened in the editor THEN the user will see a client server folder structure.
2. WHEN I run `npm run start` from the root directory THEN I find that my application should start up the backend and serve the client
3. WHEN I run the text editor application from my terminal THEN I find that my JavaScript files have been bundled using webpack
4. WHEN I run my webpack plugins THEN I find that I have a generated HTML file, service worker, and a manifest file.
5. WHEN I use next-gen JavaScript in my application THEN I find that the text editor still functions in the browser without errors.
6. WHEN I open the text editor THEN I find that IndexedDB has immediately created a database storage.
7. WHEN I enter content and subsequently click off of the DOM window THEN I find that the content in the text editor has been saved with IndexedDB.
8. WHEN I reopen the text editor after closing it THEN I find that the content in the text editor has been retrieved from our IndexedDB.
9. WHEN I click on the Install button THEN I download my web application as an icon on my desktop.
10. WHEN I load my web application THEN I should have a registered service worker using workbox.
11. WHEN I register a service worker THEN I should have my static assets pre cached upon loading along with subsequent pages and static assets.
12. WHEN I deploy to Heroku THEN I should have proper build scripts for a webpack application.


<br>
<br>

### About ###

---

<br>

1. WHEN the application is opened in the editor THEN the user will see a client server folder structure.
  > The application uses a client server folder structure to partition out the client files from the server files.

2. WHEN I run `npm run start` from the root directory THEN I find that my application should start up the backend and serve the client
  > the stript npm run start will build the production webpack files and then start the server on the specified port to begin serving the application.

3. WHEN I run the text editor application from my terminal THEN I find that my JavaScript files have been bundled using webpack
  > Using the npm run client will run the webpack scripts to bundle the htmk, css, and js files to be served to the user in development mode.

4. WHEN I run my webpack plugins THEN I find that I have a generated HTML file, service worker, and a manifest file.
  > Using the npm run client will bundle and generate an html file, service worker, and a manifest file in the dist directory to be served to the client.

5. WHEN I use next-gen JavaScript in my application THEN I find that the text editor still functions in the browser without errors.
  > The text editor functions in the browser both on and offline.

6. WHEN I open the text editor THEN I find that IndexedDB has immediately created a database storage.
  > The editor uses indexedDB for client side storage of the text in the editor. 

7. WHEN I enter content and subsequently click off of the DOM window THEN I find that the content in the text editor has been saved with IndexedDB.
  > When the user clicks off the editor, the putDB function is called which takes the editor content and puts it to the indexedDB under the id of 1. 

8. WHEN I reopen the text editor after closing it THEN I find that the content in the text editor has been retrieved from our IndexedDB.
  > When the editor is opened, a get call is made to the indexedDB and retireves the prior text. If nothing is found in the DB, the editor will fall back to local storage, if nothing is present in local storage, the header is loaded to the editor.

9. WHEN I click on the Install button THEN I download my web application as an icon on my desktop.
  > When the install button is clicked the user is prompted to respond if they wish to install the application. If yes, and icon is placed on the desktop for offline use.

10. WHEN I load my web application THEN I should have a registered service worker using workbox.
  > Service workers are built per the manifest and used for asset caching of the static files and icons.

11. WHEN I register a service worker THEN I should have my static assets pre cached upon loading along with subsequent pages and static assets.
  > Assets are pre cached when initially loaded online, and used for when the network is unavailable, allowing for offline use.

12. WHEN I deploy to Heroku THEN I should have proper build scripts for a webpack application.
  > App succesfully deploys and launches on Heroku.
<br>
<br>

### Screenshots ###

---

N/A

<br>

### Links ###

---

<br>


Link to Github repo: https://github.com/JDReeves86/ideal-potato-JATE

Link to Heroku app: 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

---

---

## Assignment Details & Grading Rubric ##

---

---

<br>
<br>



# 19 Progressive Web Applications (PWA): Text Editor

## Your Task

As you have progressed through this course, you have put together a number of impressive projects that you can show off to potential employers. This project is no exception; in fact, it features some of the most impressive expressions of the concepts you have learned so far.

Your task is to build a text editor that runs in the browser. The app will be a single-page application that meets the PWA criteria. Additionally, it will feature a number of data persistence techniques that serve as redundancy in case one of the options is not supported by the browser. The application will also function offline.

To build this text editor, you will start with an existing application and implement methods for getting and storing data to an IndexedDB database. You will use a package called `idb`, which is a lightweight wrapper around the IndexedDB API. It features a number of methods that are useful for storing and retrieving data, and is used by companies like Google and Mozilla.

You will deploy this full-stack application to Heroku using the [Heroku Deployment Guide on The Full-Stack Blog](https://coding-boot-camp.github.io/full-stack/heroku/heroku-deployment-guide).

## User Story

```md
AS A developer
I WANT to create notes or code snippets with or without an internet connection
SO THAT I can reliably retrieve them for later use
```

## Acceptance Criteria

```md
GIVEN a text editor web application
WHEN I open my application in my editor
THEN I should see a client server folder structure
WHEN I run `npm run start` from the root directory
THEN I find that my application should start up the backend and serve the client
WHEN I run the text editor application from my terminal
THEN I find that my JavaScript files have been bundled using webpack
WHEN I run my webpack plugins
THEN I find that I have a generated HTML file, service worker, and a manifest file
WHEN I use next-gen JavaScript in my application
THEN I find that the text editor still functions in the browser without errors
WHEN I open the text editor
THEN I find that IndexedDB has immediately created a database storage
WHEN I enter content and subsequently click off of the DOM window
THEN I find that the content in the text editor has been saved with IndexedDB
WHEN I reopen the text editor after closing it
THEN I find that the content in the text editor has been retrieved from our IndexedDB
WHEN I click on the Install button
THEN I download my web application as an icon on my desktop
WHEN I load my web application
THEN I should have a registered service worker using workbox
WHEN I register a service worker
THEN I should have my static assets pre cached upon loading along with subsequent pages and static assets
WHEN I deploy to Heroku
THEN I should have proper build scripts for a webpack application
```

## Mock-Up

The following animation demonstrates the application functionality:

![Demonstration of the finished Module 19 Challenge being used in the browser and then installed.](./Assets/00-demo.gif)

The following image shows the application's `manifest.json` file:

![Demonstration of the finished Module 19 Challenge with a manifest file in the browser.](./Assets/01-manifest.png)

The following image shows the application's registered service worker:

![Demonstration of the finished Module 19 Challenge with a registered service worker in the browser.](./Assets/02-service-worker.png)

The following image shows the application's IndexedDB storage:

![Demonstration of the finished Module 19 Challenge with a IndexedDB storage named 'jate' in the browser.](./Assets/03-idb-storage.png)

## Grading Requirements

> **Note**: If a Challenge assignment submission is marked as “0”, it is considered incomplete and will not count towards your graduation requirements. Examples of incomplete submissions include the following:
>
> * A repository that has no code
>
> * A repository that includes a unique name but nothing else
>
> * A repository that includes only a README file but nothing else
>
> * A repository that only includes starter code

This Challenge is graded based on the following criteria:

### Technical Acceptance Criteria: 40%

* Satisfies all of the above acceptance criteria plus the following:

  * Uses IndexedDB to create an object store and includes both GET and PUT methods

  * The application works without an internet connection

  * Automatically saves content inside the text editor when the DOM window is unfocused

  * Bundled with webpack

  * Create a service worker with workbox that Caches static assets

  * The application should use babel in order to use async / await

  * Application must have a generated `manifest.json` using the `WebpackPwaManifest` plug-in

  * Can be installed as a Progressive Web Application

### Deployment: 32%

* Application deployed to Heroku at live URL with build scripts

* Application loads with no errors

* Application GitHub URL submitted

* GitHub repo contains application code

### Application Quality: 15%

* Application user experience is intuitive and easy to navigate

* Application user interface style is clean and polished

* Application resembles the mock-up functionality provided in the Challenge instructions

### Repository Quality: 13%

* Repository has a unique name

* Repository follows best practices for file structure and naming conventions

* Repository follows best practices for class/id naming conventions, indentation, quality comments, etc.

* Repository contains multiple descriptive commit messages

* Repository contains quality README file with description, screenshot, and link to deployed application

## Review

You are required to submit the following for review:

* The URL of the deployed application

* The URL of the GitHub repository, with a unique name and a README describing the project

- - -
© 2022 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
