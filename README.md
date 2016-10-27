Demo PouchDB + Ionic 2 RC + TypeScript 2
=====

A demo app to show how to use PouchDB with Ionic 2 and TypeScript.

The app was created using:

```bash
npm install -g ionic
ionic start test --v2 
cd test
```

Then PouchDB was installed using:

```bash
npm install --save pouchdb
```

The I made modifications to the default Ionic app:

Importing PouchDB:

```typescript
// src/app/app.component.ts
import PouchDB from 'pouchdb';
console.log("Hey look, I've got PouchDB:", PouchDB);
let db = new PouchDB('database');
console.log("Hey look, I've got a PouchDB database:", db);
```

Then I started the app:

```bash
ionic serve
```

In your browser console, you should see "Hey look, I've got PouchDB" and "Hey look, I've got a
PouchDB database".


