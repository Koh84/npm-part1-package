# npm

https://www.youtube.com/watch?v=J4b_T-qH3BY

create folder
1. package
2. test-folder

cd package
init a git repo...

npm init
enter the package details etc

create index.js and add the code
function isWds(string) {
    return string === 'WDS'
}

module.exports = isWds

npm link

go to cd test-folder
create a "script.js" and add the code 

const isWds = require('is-wds');
console.log(isWds('WDS'));

then type
npm link is-wds


to run test, enter code
node .\script.js

then cd back to package
npm publish - you also need npm account

if you are not log in to npm, do the following,
npm login

npm publish 

if we get npm ERR! code E403
verify your email

if you change your package.json name to use your own namespace or scoped package
@kelvinkoh/is-wds
do the following
npm publish --access-public

npm init --scope=kelvinkoh to automate the above
