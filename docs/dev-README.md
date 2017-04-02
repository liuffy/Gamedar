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

### Wireframes 
![Wireframe1](http://res.cloudinary.com/liuffy/image/upload/v1491088803/gamedar-wireframe-1_jmfsnw.png)  
![Wireframe2](http://res.cloudinary.com/liuffy/image/upload/v1491088803/gamedar-wireframe-article_ncaxqk.png)  

## Technologies & Technical Challenges 

### Technologies

This extension will be implemented using **Javascript, HTML, and CSS**. In addition, it uses **React/Redux** to handle state, and **Firebase** to construct a realtime, cloud-hosted database. 

Authentification will also be supported by Firebase. 

There will be several React components used to build this website: 

- `GameSearch`: will be the search bar for submitting queries on specific names of video games
- `DropDownMenu`: the drop down menu component for the `Genre` and `Platform` buttons
- `NewsIndex`: will display either all results or results filtered by genre or platform. 
  - `NewsIndex` will contain an unordered list of `NewsIndexItem`s for each of the results.
  - It will also contain `ReleaseDateIndex`, a list of games and their upcoming release dates, ordered by how soon they will be released.

### Technical Challenges

* Configuring Firebase
* Aggregating data from multiple gaming APIs - will they all have the endpoints needed to be usable?
* How to avoid posting repeat articles?


## Implementation Timeline

**Part 1: Learning, Tutorialing**
* Learn how to implement Firebase by completing [this tutorial](https://www.airpair.com/firebase/posts/firebase-building-realtime-app)
* Set up React file structure, package.json and Firebase forge for app

By the end of the day, the project folder will have: 
- [X] Completed tutorial 
- [ ] `React` file structure
- [X] `package.json` - contains dependencies (i.e. babel-core, react, redux, etc.)
- [X] `.gitignore` file
- [ ] `webpack.config.js` - webpack bundling file
  - [ ] Add main entry point of the extension.
- [ ] Set up Firebase Forge
 
**Part 2: API Wrapping, Testing, Aggregating** 
* Research geolocation API and Yelp API.
* Deploy skeleton on Heroku 

By the end of the day, I should have:
- [ ] Figured out how to get results from each of the APIs by genre, platform, and name (and figured out if all are usable)
- [ ] Configured Firebase database
- [ ] Deployed draft of app on Heroku


**Part 3: Redux Cycles - Part 1**
* Create utils for API calls, action creators, reducers, redux store.
- [ ] `news_utils.js` - handle queries for APIs
  - [ ] Test API calls in Dev Tools 
- [ ] `news_actions.js` - action creators 
- [ ] `news_reducer.js` - process action.data
- [ ] `root_reducer.js` - gathers child reducers' results into single state object
- [ ] `store.js` - holds the whole state tree of the app

**Part 4: Redux Cycles - Part 2 (Rendering!)**
* Create components for extension.
- [ ] `root.jsx` - Figure out routing 
- `DropDownMenu`: the drop down menu component for the `Genre` and `Platform` buttons
- [ ] `GameSearch`: Input form for submitting queries
- [ ] `NewsIndex`: (Index) will display all results 
  - [ ] contains an unordered list of `NewsIndexItem`s for each of the results
- [ ] `NewsModal`: modal that dynamically renders the article that the user clicks on

**Part 5: Clean up and Deploy**
- [ ] Final styling - make sure all components are aesthetically consistent
- [ ] Clean up code in all files
- [ ] Remove any unused dependencies listed in `package.json` file
- [ ] Check how page looks in all modern browsers

## Stylistic Elements I want to use/feature: 
- [ ] Drop-down menu
- [ ] Responsive layout (Masonry, responsive grid based on percentages, media queries)
- [ ] "Load more" button (Preferable for [reasons](https://www.smashingmagazine.com/2016/03/pagination-infinite-scrolling-load-more-buttons/))

