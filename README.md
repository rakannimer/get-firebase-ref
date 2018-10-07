# Get Firebase Ref

[![CircleCI][circleci-badge]][circleci-href]
[![NPM][npm-version-badge]][npm-href]
[![BundlePhobia][bundlephobia-badge]][bundlephobia-href]

Get a Firebase ref to a firebase node from a query and firebase module (web, react-native or admin)

## Install

```sh
  yarn add get-firebase-ref
```

## Usage

Provides getFirebaseRef function as default and named exports

```typescript
import { getFirebaseRef } from "get-firebase-ref";
import getFirebaseRef from "get-firebase-ref";
import firebase from "firebase/app";
import "firebase/database";

const ref = getFirebaseRef({ firebase, path: "posts/", limitToFirst: 10 });
```

## API

### Input

A Firebase Query :

```typescript
export interface FirebaseQuery {
  firebase?: any;
  path: string;
  orderByChild?: null | string;
  orderByKey?: null | any;
  orderByValue?: null | any;
  limitToFirst?: null | number;
  limitToLast?: null | number;
  startAt?: null | number;
  endAt?: null | number;
  equalTo?: null | any;
  keysOnly?: boolean;
  once?: boolean;
  isList?: boolean;
}
```

### Output

A Firebase ref

[circleci-href]: https://circleci.com/gh/rakannimer/get-firebase-ref
[circleci-badge]: https://img.shields.io/circleci/project/github/rakannimer/get-firebase-ref.svg
[npm-href]: https://www.npmjs.com/package/get-firebase-ref
[npm-version-badge]: https://img.shields.io/npm/v/get-firebase-ref.svg
[npm-license-badge]: https://img.shields.io/github/license/rakannimer/get-firebase-ref.svg
[bundlephobia-badge]: https://img.shields.io/bundlephobia/minzip/get-firebase-ref.svg
[bundlephobia-href]: https://bundlephobia.com/result?p=get-firebase-ref
