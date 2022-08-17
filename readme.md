# demo how to use lerna with npm
## test environment
node@14.15.1
npm@6.14.8

## init
If init with 'lerna init', remember to change below:
1. config 'packages' and 'useWorkspaces=false' in lerna.json
2. remove 'workspaces' config in package.json  
Reference: https://lerna.js.org/docs/api-reference/configuration   
workspace only works with yarn, it is default option for `lerna init`.

## list
```
> npx lerna list
lerna notice cli v5.4.2
footer
header
mix
lerna success found 3 packages
```
if the found packages number is 0, check configurations!

## bootstrap
```
npx lerna bootstrap
```
it will run 'npm install in each sub package, and link local depends.

## run
```
npm lerna run build
```
it will run 'npm run build' in each sub pacakge if it has such 'build script'.

## publish
```
npm lerna publish
npm lerna publish --registry=<url>
```
1. workspace should be clean
2. it will bump up version in lerna.json, and change version for all packages
3. it will commit, tag, and push to remote git
4. it will publish package to registry

## clean
```
npx clean
```
remove all node_modules in all packages.
If you want to also clean git status:
```
git clean -xfd
git reset --hard
```


## other commands
https://lerna.js.org/docs/api-reference/commands