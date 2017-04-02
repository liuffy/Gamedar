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

* Configuring Firebase
* Aggregating data from multiple gaming APIs - will they all have the endpoints needed to be usable?


## Implementation Timeline

**Day 1: Learning, Tutorialing**
* Learn how to implement Firebase by completing [this tutorial](https://www.airpair.com/firebase/posts/firebase-building-realtime-app)
* Set up React file structure, package.json and Firebase forge for app

By the end of the day, the project folder will have: 
- [X] Completed tutorial 
- [ ] `React` file structure
- [ ] `package.json` - contains dependencies (i.e. babel-core, react, redux, etc.)
- [ ] `webpack.config.js` - webpack bundling file
  - [ ] Add main entry point of the extension.
- [ ] Set up Firebase Forge
 
**Day 2: API Wrapping, Testing, Aggregating** 
* Research geolocation API and Yelp API.
* Deploy skeleton on Heroku 

By the end of the day, I should have:
- [ ] Figured out how to get results from each of the APIs by genre, platform, and name (and figured out if all are usable)
- [ ] Deployed draft of app on Heroku


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


**Day 7: Deploying and distribution**
- [ ] Compress extension folder into a .zip file. 
- [ ] Add new item on the developer dashboard.
- [ ] Share link to Google Chrome extension and demo page on Facebook, Tumblr, and Reddit. 

