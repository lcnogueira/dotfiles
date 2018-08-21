# eslint-prettier-config

My ESLint and Prettier config (and other stuff).

## Why did I create this?

To recap what my prefered configurations are :).

## How to use it

1. Install `eslint` and `babel-eslint` **locally** (a matter of preference) as dev dependencies:

```
npm i eslint babel-eslint --save-dev
```

2. Install plugins for [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) at VSCode.

3. Create [.eslintrc](./.eslintrc) in the project root folder.

4. Insert the config in [settings.json](./settings.json) file (`Ctrl + ,` to open the file).
P.S.: Insert the above config in `workspace settings`, so that it overrides `user settings`.

5. That's all! Have fun!

## Run ESLint in the entire project (optional):

```
  ./node_modules/.bin/eslint .
```

If you prefer, insert a script in `package.json`, so that you can run `npm run lint`:

```
"lint": "./node_modules/.bin/eslint ."
```

## Run Prettier on all JS Files (optional):
You can use this in case you have already started your project and yous JS files are not in format you wish to.
```
npm i prettier --save-dev
./node_modules/.bin/prettier --single-quote --semi --trailing-comma es5 --write "**/*.js"
```

If you prefer, insert a script in `package.json`, so that you can run `npm run format-prettier`:
```
"format-prettier": "./node_modules/.bin/prettier --single-quote --semi --trailing-comma es5 --write \"**/*.js\""
```
