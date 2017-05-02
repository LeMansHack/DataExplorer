# LeMans Hack Dataexplorer for test data

This repo contains recorded LeMans test data from the run in 2014. You can use the `dataexplorer` API to retrieve the data.

## Installation

Add it to your project by using Yarn:

````
yarn add https://github.com/LeMansHack/DataExplorer.git
````

Or by using NPM:

```
npm install https://github.com/LeMansHack/DataExplorer.git
```

## Usage

When added you can require the dataexplorer to retrieve the data by using the following code:

```javascript
let DataExplorer = require('dataexplorer');
let second = 0;

setInterval(() => {
  let data = DataExplorer.getData(second);
  second += 1;
}, 1000):
```

Because all data is recorded by timestamp, seconds is used to count up the data from second 0.

You can also get a specific file by it´s timestamp using `DataExplorer.getFileData(timestamp)`.