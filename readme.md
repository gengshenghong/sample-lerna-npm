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


## other commands
https://lerna.js.org/docs/api-reference/commands