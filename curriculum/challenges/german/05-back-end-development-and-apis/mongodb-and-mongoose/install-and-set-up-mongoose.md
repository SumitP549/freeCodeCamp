---
id: 587d7fb6367417b2b2512c06
title: Installieren und Einrichten von Mongoose
challengeType: 2
forumTopicId: 301540
dashedName: install-and-set-up-mongoose
---

# --description--

Working on these challenges will involve you writing your code using one of the following methods:

- Clone <a href="https://github.com/freeCodeCamp/boilerplate-mongomongoose/" target="_blank" rel="noopener noreferrer nofollow">this GitHub repo</a> and complete these challenges locally.
- Use <a href="https://replit.com/github/freeCodeCamp/boilerplate-mongomongoose" target="_blank" rel="noopener noreferrer nofollow">our Replit starter project</a> to complete these challenges.
- Verwende einen Site-Builder deiner Wahl, um das Projekt fertigzustellen. Be sure to incorporate all the files from our GitHub repo.

Wenn du fertig bist, stelle sicher, dass dein Projekt öffentlich zugänglich gehostet ist. Gib dann die URL in das `Solution Link`-Feld ein.

In dieser Aufgabe wirst du eine MongoDB-Atlas-Datenbank einrichten und die erforderlichen Pakete importieren, um sich mit ihr zu verbinden.

Follow <a href='https://www.freecodecamp.org/news/get-started-with-mongodb-atlas/' target="_blank" rel="noopener noreferrer nofollow">this tutorial</a> to set up a hosted database on MongoDB Atlas.

# --instructions--

`mongoose@^5.11.15` has been added to your project’s `package.json` file. First, require mongoose as `mongoose` in `myApp.js`. Next, create a `.env` file and add a `MONGO_URI` variable to it. Its value should be your MongoDB Atlas database URI. Be sure to surround the URI with single or double quotes, and remember that you can't use spaces around the `=` in environment variables. For example, `MONGO_URI='VALUE'`.

**Note:** If you are using Replit, you cannot create a `.env` file. Instead, use the built-in <dfn>SECRETS</dfn> tab to add the variable. <em>Do not</em> surround the values with quotes when using the <em>SECRETS</em> tab.

When you are done, connect to the database using the following syntax:

```js
mongoose.connect(<Your URI>, { useNewUrlParser: true, useUnifiedTopology: true });
```

# --hints--

Abhängigkeit "mongoose Version ^5.11.15" sollte sich in package.json befinden

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/file/package.json').then(
    (data) => {
      var packJson = JSON.parse(data);
      assert.property(packJson.dependencies, 'mongoose');
      assert.match(
        packJson.dependencies.mongoose,
        /^\^5\.11\.15/,
        'Wrong version of "mongoose". It should be ^5.11.15'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

"mongoose" sollte mit einer Datenbank verbunden sein

```js
(getUserInput) =>
  $.get(getUserInput('url') + '/_api/is-mongoose-ok').then(
    (data) => {
      assert.isTrue(data.isMongooseOk, 'mongoose is not connected');
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--

```js
/**
  Backend challenges don't need solutions, 
  because they would need to be tested against a full working project. 
  Please check our contributing guidelines to learn more.
*/
```
