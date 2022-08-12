<h1 align="center">Geokit doc</h1>


A CLI tool which helps to made mapping  work efeciently!!

## Installation and Usage

The steps below will walk you through setting up your own instance of Geokit documentation.

### Install Project Dependencies
To set up the development environment for this website, you'll need to install the following on your system:

- [Node](http://nodejs.org/) v8 (To manage multiple node versions we recommend [nvm](https://github.com/creationix/nvm))
- [Yarn](https://yarnpkg.com/) Package manager

### Install Application Dependencies

If you use [`nvm`](https://github.com/creationix/nvm), activate the desired Node version:

```
nvm install
```

Install Node modules:

```
npm install
```


### Starting the app

```
yarn run serve
```

### Deploy

```
yarn run deploy
```

Compiles the sass files, javascript, and launches the server making the site available at `http://localhost:3000/`
The system will watch files and execute tasks whenever one of them changes.
The site will automatically refresh since it is bundled with livereload.

# Deployment
To prepare the app for deployment run:

```
yarn run build
```

This will package the app and place all the contents in the `dist` directory.
The app can then be run by any web server.
