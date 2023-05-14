---
title: Fastest way to check if an object is empty
category: Frontend Cheetseat
date: 2021-10-27
tags: ['object', 'JavaScript']
author: Suresh Kumar Mukhiya
thumbnailText: 'Is object empty?'
---

### Problem:

Given an object, the aim is to check weather the object is empty or not.

### Input:

```javascript
const data = {}
```

### Expected Output:

```javascript
isObjectEmpty({}) => TRUE
isObjectEmpty({a: 1}) => FALSE
```

### Solution:

Note, there are several ways to check weather an object is EMPTY or not. The solution given below is one of the fastest way to check it.

Check benchmarking here: https://tomekkolasa.com/how-to-check-if-object-is-empty-in-javascript.

```javascript
/**
 * There is one of the fastest way to check if an object is Empty
 */

export const isObjectEmpty = (myObject = {}): boolean => {
  for (const prop in myObject) {
    if (Object.prototype.hasOwnProperty.call(myObject, prop)) {
      return false
    }
  }
  return true
}
```
