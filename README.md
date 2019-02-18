# Start from scratch

```bash
yarn add firebase-tools --global
mkdir project
cd project
yarn init -y
```

Add the next dependencies:

```bash
yarn add react react-dom next@7.0.2 firebase-admin firebase-functions
yarn add @babel/cli @babel/core @babel/preset-env cpx --dev
```

in package.json add scripts for build project:

```js
  "scripts": {
    "dev": "next",
    "next": "next build",
    "build": "babel src/functions -d functions",
    "copy": "cpx \"*{package.json,yarn.lock}\" \"functions\" && yarn",
    "deploy": "firebase deploy",
    "function": "firebase deploy --only functions"
  }
```