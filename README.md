# Logger Setup for NodeJS App
This is a simple logger set up that enables you to quickly set up the logger. This setup uses the popular awseome libraries [winston](https://www.npmjs.com/package/winston) and [winston-daily-rotate-file](https://www.npmjs.com/package/winston-daily-rotate-file)

## Features
* Daily logging files to app-logs/
* Log file name and line number

## Install dependencies
```
npm i -S winston winston-daily-rotate-file
```
## Copy logger.js to your app
copy the logger.js file in this repository to your applications folder.

## Setting the root paths
make sure you are pointing to the right folders. Modify the below lines if you placed the logger.js file or app-logs/ in different locations than the root folder

```
...
const PROJECT_ROOT = path.join(__dirname)
const LOGS_ROOT = path.join(__dirname, 'app-logs')
...
```

## logging
If you are using the logger in index.js, from line 33,
The logger would effect logging into app-logs/<YYYY-MM-DD>.log file. Along with the file name and line number
```
logger.info('Started logging')

```

log:
```
2017-04-01T09:17:40.443Z - info: index.js : 33 Started logging
```

Happy Logging!