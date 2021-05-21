# **vuejs-gh-pages**

## Description

---

Sample Vue.js project which is deployed as Github Pages

- [Vue.js](https://cli.vuejs.org/guide/prototyping.html)
- [GH-Pages](https://www.npmjs.com/package/gh-pages)

View the application - [https://neographer.github.io/vuejs-gh-pages/]

## Steps to create this project

---

### 1. Vue.js Boilerplate

```bash
npm install -g @vue/cli
vue new vuejs-gh-pages
```

### 2. Start the application

```bash
cd vuejs-gh-pages
npm install
npm run serve
```

### 3. Enable gh-pages

- Install the npm package
  -- `npm install gh-pages --save-dev`
- Create new `vue.config.js` and add the following code <br>

  ```javascript
  module.exports = {
    publicPath:
      process.env.NODE_ENV === "production" ? "/vuejs-gh-pages/" : "/",
  };
  ```

  > Where `"/vuejs-gh-pages/"` is the name of the repository.

- Update the scripts section with following line
  ```json
  "scripts": {
    "deploy": "gh-pages -d dist"
  }
  ```

### 4. Build and Deploy

- Build the application
  ```bash
  npm run build
  ```
- Deploy the application

  ```bash
  npm run deploy
  ```

  or

  ```bash
  gh-pages -d dist
  ```
