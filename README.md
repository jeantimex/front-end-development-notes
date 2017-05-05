# Front End Development Notes

Some notes about front end development in case I forget.

## Creating an ES6 project

There are two different ways, one is to use `babel-node`, and the other is `babel-register`. In order to use `babel-node`, you should install `babel-cli` and configure `.babelrc` to include babel presets, normally `babel-preset-es2015`.

### Method 1. Use babel-node

Step 1. Create a project folder and initialize with npm
```
$ mkdir es6-project
$ cd es6-project
$ npm init -y
```

Step 2. Install `babel-cli` and `babel-preset-es2015`
```
$ npm install --save-dev babel-cli babel-preset-es2015
```

Step 3. Configure `.babelrc`
```
$ touch .babelrc
$ echo "{ \"presets\": [\"es2015\"] }" >> .babelrc
```

Step 3. Write some ES6 codes
```
$ touch app.js
$ echo "const a = 7;" >> app.js
```

Step 4. Run the script!
```
$ babel-node app.js
```
### Method 2. Use babel-register

Step 1. Create a project folder and initialize with npm
```
$ mkdir es6-project
$ cd es6-project
$ npm init -y
```

Step 2. Install `babel-register`
```
$ npm install --save-dev babel-register
```

Step 3. Write some ES6 codes
```
$ touch app.js
$ echo "const a = 7;" >> app.js
```
Step 4. Write entry point
```
touch entry.js
$ echo "require('babel-register');require('./app.js');" >> entry.js
```

Step 5. Run the scripts
```
$ node entry.js
```
