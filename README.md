# vue-account-form

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Heroku Deployment

``` bash
# Create a new application no Heroku
heroku create <application_name>

# Add heroku Git remote repository
heroku git:remote -a <application_name>

# Configure Heroku buildpack
heroku buildpacks:set heroku/nodejs

# Build for production and push/deploy on Heroku
npm run deploy
```

The application is available at: https://<application_name>.herokuapp.com/, such as [https://vue-account-form.herokuapp.com/](https://vue-account-form.herokuapp.com/).
