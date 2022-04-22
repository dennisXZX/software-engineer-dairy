### What happen when you run `npm run xxx`?

- It would first look at current project `node_modules/.bin` for the program
- If the program cannot be found there, it would start to look at global `node_modules/.bin` (package installed by `npm i -g`)
- If the program cannot be found there, it would look at `$PATH` to see if the program is there
