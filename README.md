# observable-fs
Observable node `fs` functions respecting the nodejs API.

## Install
```
npm install --save @lutangar/observable-fs
```

## Usage
```
const { writeFile } = require('@lutangar/observable-fs');

writeFile('foo.txt', 'bar')
.concat(
    readFile('foo.txt')
    .do(content => console.log(content.toString('utf8')))
);
```

## Resources
* https://nodejs.org/api/fs.html
* http://reactivex.io/rxjs/class/es6/Observable.js~Observable.html

## Licence
MIT