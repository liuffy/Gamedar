# Open

![Gamedar logo](http://res.cloudinary.com/liuffy/image/upload/c_scale,w_216/v1491088889/gamedar-logo2_cb0lgo.png)

### Purpose 

Gamedar is a full-stack, single page newsfeed website (made with React/Redux and Firebase) for news and release dates for video games. It will make it easy for users to check for release dates and articles from multiple databases (Steam, IGDB, Giant Bomb) all in one page. 


## Background

While there are many gaming news sites (such as [Polygon](http://www.polygon.com/)), most of them have a dense layout that makes it hard to search for games belonging to a specific genre or platform. 

**Gamedar** aims to get the latest news by either genre or platform within two clicks.

### Functionality and MVP

With this extension, users will be able to:

- [ ] Check for release dates and news about video games, either in aggregated form or by genre or platform.
- [ ] Search for release dates or news articles for a *specific game* in the search bar.
- [ ] Add comments on newsArticle objects, which will be immediately displayed at the bottom of the article. 
  - [ ] This will require the user to create an account (however, all content is viewable without authentification of any sort)


### Wireframes 
![Wireframe1](http://res.cloudinary.com/liuffy/image/upload/v1491088803/gamedar-wireframe-1_jmfsnw.png)  
![Wireframe2](http://res.cloudinary.com/liuffy/image/upload/v1491088803/gamedar-wireframe-article_ncaxqk.png)  

## Technologies & Technical Challenges 

### Technologies

This extension will be implemented using **Javascript, HTML, and CSS**. In addition, it uses **React/Redux** to handle state, and **Firebase** to construct a realtime, cloud-hosted database. 

Authentification will also be supported by Firebase. 

There will be several React components used to build this website: 

- `GameSearch`: will be the search bar for submitting queries on specific names of video games
- `NewsIndex`: will display either all results or results filtered by genre or platform. 
  - `NewsIndex` will contain an unordered list of `NewsIndexItem`s for each of the results.
  - It will also contain `ReleaseDateIndex`, a list of games and their upcoming release dates, ordered by how soon they will be released.

### Technical Challenges

* 
* 

## Implementation Timeline

**Day 1: Learning, Tutorialing**
* Learn the essential infrastructure of a Chrome Extension by following the [tutorial provided by Google Chrome.](https://developer.chrome.com/extensions/getstarted). Build a test extension in a separate folder. 
* Do some research on purpose and structure of a `manifest.json` file. 
* Then, start building the infrastructure for personal extension. By the end of the day, the project folder will will have:

- [X] A completed `package.json`
- [X] A completed `manifest.json`
- [?] Script for Google Analytics 

**Day 2: Basic UI, Geolocation API, Yelp API**
* Add main entry point of the extension. 
* Flesh out basic UI.
* Research geolocation API and Yelp API.

By the end of the day, the project folder will have:
- [X] `popup.html` - main entry point of the app as defined in the manifest file.
- [X] `popup.js` - use javascript file by the [the Chromium Authors](http://the-chromium-authors.software.informer.com/)
- [X] `webpack.config.js` - webpack bundling file
- [X] `package.json` - contains dependencies (i.e. babel-core, react, redux, etc.)

**Day 3: Redux Cycles - Part 1**
* Create utils for API calls, action creators, reducers, redux store.
- [X] `yelp_api_utils.js` - handle queries for Yelp API
  - [X] Test API calls in Dev Tools 
- [X] `yelp_actions.js` - action creators 
- [X] `result_reducer.js` - process action.data
- [X] `root_reducer.js` - gathers child reducers' results into single state object
- [X] `store.js` - holds the whole state tree of the app

**Day 4: Redux Cycles - Part 2 (Rendering!)**
* Create components for extension.
- [X] `root.jsx` - Figure out routing 
- [X] `SearchForm`: will be the input form for submitting queries
- [X] `ResultList`: (index) will display all results 
  - [X] contains an unordered list of `ResultIndexItem`s for each of the results
- [X] `ResultShow`: provides additional information about the business (i.e. address/#)

**Day 6: CSS Styling, demo page for chrome extension** 

By the end of the day:
- [X] Have components/HTML styled nicely using CSS.
- [X] Create icon for extension
- [ ] Set up github page for the extension.
- [ ] Mock up wireframes for how the demo page will look 
- [X] Grab nice looking screenshots from the chrome extension
- [ ] Make a few gifs that shows off the key features of the chrome extension

**Day 7: Deploying and distribution**
- [ ] Compress extension folder into a .zip file. 
- [ ] Add new item on the developer dashboard.
- [ ] Share link to Google Chrome extension and demo page on Facebook, Tumblr, and Reddit. 


### Plan for getting users and reviews

- Will share link to Google Chrome extension in: 
- [ ] Facebook groups such as:
  - [X] **Techy Wendy** (Tech-focused group for Wellesley College alumni) 
  - [ ] **Community** (large Facebook group for Wellesley College alumni) 
  - [ ] **Wellesley By the Bay** (Facebook group for Wellesley alumni living in the bay area) 
  - [ ] General Facebook page
- [ ] Reddit forums such as:
  - [X] **/r/chrome_extensions/**
  - [X] **/r/webdev/**
  - [X] **/r/IMadeThis/**
  - [ ] **/r/chrome/**

## Bonus Features :sparkles:

- [ ] Save favorites: Add panel that shows results for saved locations. :sparkling_heart:
- [ ] Options menu: Allow users to customize their experience by being able to choose aspects such as:
  - [ ] Whether to display time in 24-hour format or 12-hour format
  - [ ] Number of results shown for each query.