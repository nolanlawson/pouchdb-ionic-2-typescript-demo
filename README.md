Demo PouchDB + Ionic 2 + TypeScript
=====

A demo app to show how to use PouchDB with Ionic 2 and TypeScript.

The app was created using:

```bash
npm install -g ionic@beta
ionic start test --v2 --ts
cd test
```

Then PouchDB was installed using:

```bash
npm install --save pouchdb
```

The I made modifications to the default Ionic app:

```typescript
// typings/index.d.ts
declare module 'pouchdb' {
  var PouchDB: any;
  export default PouchDB;
}
```

The above is only necessary because the PouchDB DefinitelyTyped definitions are out of date (as of this writing, June 2016). Hopefully that will be fixed soon, at which point you'll be able to do `typing install pouchdb` instead.

Then I imported PouchDB:

```typescript
// app/app.ts
import * as PouchDB from 'pouchdb';
console.log("Hey look, I've got PouchDB:", PouchDB);
```

Then I started the app:

```bash
ionic serve
```

In your browser console, you shoudl see "Hey look, I've got PouchDB".


