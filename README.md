# TestCafe Starter

## Running Test
testcafe chromium helloTestcafe.js
testcafe firefox helloTestcafe.js

## Useful Commands
-b, list browsers

-s, test a screenshot whenever a test fails 
-p, screenshot path pattern 

## Reports 
### testcafe-reporter-html
npm install testcafe-reporter-html

testcafe chromium tests/helloTestcafe.js --reporter html 
    by derfault the html is written to stdout

testcafe chromium tests/helloTestcafe.js --reporter html:testResults/helloTestcafeResults.html
    specify the html output file 

### testcafe-reporter-xunit
- Build (Execute Shell)
npm install testcafe testcafe-reporter-xunit

node_modules/.bin/testcafe chromium:headless tests/**/*

cd /var/lib/jenkins/workspace/testCafe
touch *.xml

- Post Build Actions
Publish JunitTest results report
res.xml

## Broser Support 
[testcafe browser support](https://devexpress.github.io/testcafe/documentation/using-testcafe/common-concepts/browsers/browser-support.html)

### Mobile Browser Support
#### Run test on your mobile device
testcafe remote tests/helloTestcafe.js --qr-code

### Chrome Device Emulation
testcafe "chromium:emulation:device=iphone X" tests/helloTestcafe.js

## Accessability Testing 
[axe-testcafe](https://www.npmjs.com/package/axe-testcafe)
npm install axe-testcafe --save

## Run test from IDE 
### Visual Studio 
(testcafe test runner)[https://marketplace.visualstudio.com/items?itemName=romanresh.testcafe-test-runner]

## References / Documentation 
(Using TestCafe)[https://devexpress.github.io/testcafe/documentation/using-testcafe/common-concepts/browsers/using-chrome-device-emulation.html]