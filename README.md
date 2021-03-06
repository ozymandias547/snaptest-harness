# SnapTest NightwatchJS Harness

### 1. Install dependencies  

*(MacOS)*
* Install NodeJS. ( via [homebrew](https://brew.sh/) or https://nodejs.org ).
* Clone this repo `git clone <url>`
* Run `npm install` in the cloned repository
* Download [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) and copy to /usr/local/bin (or any folder that makes it available on your path)

*(Windows)*
* Install NodeJS. ( via https://nodejs.org ).  
* Clone this repo `git clone <url>`
* Run `npm install` in the cloned repository
* Download chromedriver and copy to %systemroot%\System32  (or any folder that makes it available on your ENV path)

### 2. Run via folder generation

* From the Snaptest extension, Find the dropdown menu next next to a folder and click "View Code".  Copy and run the auto-generated CLI command.  Example: `snaptest -f <folderID> -r nightwatch -s flat -t <APIkey> -a user -d me`
* Run all by typing `npm test`. 

---

Advanced usage
========
(note: SnapTest generates the tests, but you control the configuration. See available Nightwatch config at [http://nightwatchjs.org/gettingstarted#settings-file](http://nightwatchjs.org/gettingstarted#settings-file)

### Parallel tests
Configure via the nightwatch config.  See the "test_workers" config.

### Running tests in different environments and browsers
Add entries to the nightwatch.json config file to expand variations of your tests. View the [nightwatch docs about different settings.](http://nightwatchjs.org/gettingstarted#test-settings)

Running the new config setting:

```./node_modules/.bin/nightwatch --env foobarconfig```

Currently supported browsers:
1. Chrome
1. Firefox
1. Microsoft Edge

### Running single tests

After you've built a lot of tests, you may want to run only one to save time.  Use this command:
```
./node_modules/.bin/nightwatch -t test/harness.js
```
