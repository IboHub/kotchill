## kotchill.db

**NPM:** [npmjs.com/kotchill.db](https://www.npmjs.com/package/kotchill.db)

- **Persistent Storage** - Data doesn't disappear through restarts
- **Works out of the box** - No need to set up a database server, all the data is stored locally in the same project
- **Beginner Friendly** - Originally created for use in tutorials, the documentation is straightforward and jargon-free
- & more...

## Example

```js
const db = require('kotchill.db');

db.set('userInfo', { difficulty: 'Easy' })
// { difficulty: 'Easy' }

db.push('userInfo.items', 'Sword')
//{ difficulty: 'Easy', items: ['Sword'] }

db.add('userInfo.balance', 500)
//{ difficulty: 'Easy', items: ['Sword'], balance: 500 }

db.push('userInfo.items', 'Watch')
//{ difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 500 }
db.add('userInfo.balance', 500)
//{ difficulty: 'Easy', items: ['Sword', 'Watch'], balance: 1000 }

db.get('userInfo.balance') // -> 1000
db.get('userInfo.items') // ['Sword', 'Watch']
```

## Installation

**Linux & Windows**
- `npm i kotchill.db`

***Note:** Windows users may need to do additional steps [listed here](https://github.com/JoshuaWise/better-sqlite3/blob/master/docs/troubleshooting.md).*

**Mac**
1. **Install:** XCode
2. **Run:** `npm i -g node-gyp` in terminal
3. **Run:** `node-gyp --python /path/to/python2.7` (skip this step if you didn't install python 3.x)
4. **Run:** `npm i kotchill.db`
