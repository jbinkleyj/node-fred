
# node-fred &middot; [![build status](https://travis-ci.org/pastorsj/node-fred.svg?branch=master)](https://travis-ci.org/pastorsj/node-fred) [![npm version](https://img.shields.io/npm/v/node-fred.svg?style=flat)](https://www.npmjs.com/package/node-fred)
A Fred2 API wrapper

# The Fred API
[Official Documentation](https://research.stlouisfed.org/docs/api/fred/)

[Wrapper Documentation](https://pastorsj.github.io/node-fred-api/)

# Installation Instructions
```
npm install node-fred --save
```

# Example
## Using Promises
``` javascript
import Fred from 'node-fred'

const fred = new Fred(API_KEY);

function getCategory(categoryID) {
  fred.categories.getCategory(125)
    .then((res) => {
      console.log('Category', res);
    })
    .catch((err) => {
      console.error('Error', err);
    });
}
getCategory(125);
```
## Using async/await
``` javascript
import Fred from 'node-fred'

const fred = new Fred(API_KEY);

async function getCategory(categoryID) {
  try {
    const category = await fred.categories.getCategory(categoryID);
    console.log('Category', res);
  } catch (err) {
    console.error('Error', err);
  }
}
getCategory(125);
```
