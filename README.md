# Gideonnn's prettier config

My personal prettier setup for javascript projects. Feel free to use it any way you like.

## Installation

```
yarn add -D @gideonnn/prettier-config
```

Install required `peerDependencies`:

```
yarn add -D prettier
```

Import in `package.json`:

```
"prettier": "@gideonnn/prettier-config"
```

Add a format command to your `package.json`:

```
"format": "prettier --check 'src/**/*.{js,jsx,ts,tsx}'",
"format:fix": "prettier --write 'src/**/*.{js,jsx,ts,tsx}'",
```

## Enable format on save

Add the following to your `.vscode/settings.json` file:

```
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.formatOnSave": true,
```

## Add/override rules

Instead of using `package.json`, you can also import this config in your `.prettierrc.js` file. Here you can add or override rules as follows:

```
module.exports = {
  ...require("@gideonnn/prettier-config"),
  semi: false,
};
```
