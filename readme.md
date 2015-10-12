> This is a test of the Emergency Broadcast System. Important information will follow this tone.


Just testing methods of using rollup to bundle a package leveraging lodash (https://github.com/caolan/async/issues/914)

`example-direct.js` is an attempt at importing a `lodash-es` method directly (`import map from 'lodash-es/collection/map'`) while `example-main.js` attempts to load it all and cherry pick a select method.

### Results 

- `example-main.js` includes numerous unnessary dependencies and is poor at dead code removal (see [dist/example-main](./dist/example-main.js)). This is likely due to the structuring of lodash es's main file
- `example-direct.js` is quite successful at cherry-picking the required code (see see [dist/example-direct](./dist/example-direct.js))