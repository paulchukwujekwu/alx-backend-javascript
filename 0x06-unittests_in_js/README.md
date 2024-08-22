0x06-unittests_in_js

On each project folder install the following dependency:
--for mocha testing:
npm install --save-dev mocha

--for chai testing:
npm install chai

--for sinon testing:
npm install sinon

--for express application
npm install express
npm install request
npm install mocha --save-dev

then ensure to have packages.json file
cat package.json
{
  "name": "8-api",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "./node_modules/mocha/bin/mocha"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.19.2"
  },
  "devDependencies": {
    "chai": "^4.2.0",
    "mocha": "^6.2.3",
    "request": "^2.88.2",
    "sinon": "^7.5.0"
  }
}


then test your application api

root@fe52c36eb54f:~/alx-backend-javascript/0x06-unittests_in_js/10-api# npm test api.test.js

> 8-api@1.0.0 test /root/alx-backend-javascript/0x06-unittests_in_js/10-api
> ./node_modules/mocha/bin/mocha "api.test.js"



  Index page
    ✓ check correct status code (294ms)
    ✓ check correct content

  Cart page
    ✓ check correct status code for correct url (93ms)
    ✓ check correct content for correct url
    ✓ check correct status code for incorrect url (94ms)

  Available_payments page
    ✓ check correct status for correct url
    ✓ check correct body content for correct url

  Login
    ✓ check correct status code for request that's sent properly
    ✓ check correct content for request that's sent properly
    ✓ check correct status code for request that's not sent properly (94ms)


  10 passing (697ms)

root@fe52c36eb54f:~/alx-backend-javascript/0x06-unittests_in_js/10-api#

