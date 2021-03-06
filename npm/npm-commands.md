# npm commands:
-------------

```
npm init
npm init --yes


npm i <package-name>
npm install <package-name> or [npm_old_version: npm i --save <package-name>]
npm install <package-name>@x.x.x
npm install <package-name> --save-dev [dev dependencies]

npm install -g <package-name>
npm install global <package-name>


npm un <package-name>
npm uninstall <package-name>


npm list
npm list --depth=0


npm view <package-name>
npm view <package-name> dependencies
npm view <package-name> versions


npm outdated
npm -g outdated
```

HOW TO  CREATE  AND
PUBLISH NPM PACKAGE
-------------------
```
mkdir demo-lib
cd demo-lib
npm init
create -> index.js
          [module.exports.add = function(a, b) { return a+b};]

demo-lib
|
+--- index.js
|
+--- package.json

----------------(PUBLISH)
npm adduser
npm login
npm publish
```

NPM UPDATE VERSION
------------------
```
npm version major
npm version minor
npm version patch
```

EXTRA INFORMATIONS: VERSION
---------------------------
```
semantic versioning: major.minor.patch
version: 4.3.2
         [major.minor.patch]

major: change major version if the changes break the previous version
minor: add additional features that can't break the previous version
patch: change patch version if we fixed a bug


^4.2.5: 4.x.x (update: minor & patch)
~4.2.5: 4.2.x (update: patch)
 4.2.5: (exactly same version, no update)
```
