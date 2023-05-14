---
title: Insert Property and values at specific position in an Object in JavaScript
category: Frontend Cheetseat
date: 2021-12-26
tags: ['Object', 'JavaScript']
author: Suresh Kumar Mukhiya
thumbnailText: 'Insert property and value at a specific position'
---

### Problem:

Given an object, we would like to insert a property and value at spcific position.

### Input:

```javascript
const testObject = {
  id: 42,
  __EMPTY: 'EUROPRIS AS',
  __EMPTY_1: 'EUROPRIS AS',
  Apple: 'Frukt',
  __EMPTY_2: 7270424,
  Eiendomsrapport: 43831,
  __EMPTY_3: 44197,
  __EMPTY_4: 'MASKINFORSIKRING',
  __EMPTY_5: 'STASJ.ELEKTR.UTSTYR 1.RISIKO',
  __EMPTY_6: '256 EUROPRIS BUTIKKER',
  __EMPTY_7: '',
  __EMPTY_8: 76800000,
  __EMPTY_9: 27648,
  __EMPTY_10: 0
}
```

And say, we want to insert a property and value `__CUSTOM_1: 33434` between `__EMPTY_7` and ``__EMPTY_8`.

### Expected Output:

```javascript
const testObject = {
    "id": 42,
    "__EMPTY": "EUROPRIS AS",
    "__EMPTY_1": "EUROPRIS AS",
    "Apple": 'Frukt',
    "__EMPTY_2": 7270424,
    "Eiendomsrapport": 43831,
    "__EMPTY_3": 44197,
    "__EMPTY_4": "MASKINFORSIKRING",
    "__EMPTY_5": "STASJ.ELEKTR.UTSTYR 1.RISIKO",
    "__EMPTY_6": "256 EUROPRIS BUTIKKER",
    "__EMPTY_7": "",
    "__CUSTOM_1": 33434
    "__EMPTY_8": 76800000,
    "__EMPTY_9": 27648,
    "__EMPTY_10": 0
}
```

### Solution:

```javascript
const addToObject = function (obj, key, value, index) {
  // Create a temp object and index variable
  var temp = {}
  var i = 0

  // Loop through the original object
  for (var prop in obj) {
    if (Object.prototype.hasOwnProperty.call(obj, prop)) {
      // If the indexes match, add the new item
      if (i === index && key && value) {
        temp[key] = value
      }

      // Add the current item in the loop to the temp obj
      temp[prop] = obj[prop]

      // Increase the count
      i++
    }
  }

  // If no index, add to the end
  if (!index && key) {
    Object.assign(temp, { [key]: value })
  }

  return temp
}
```

## Usage

- To insert an item to the end the object, `addToObject(obj, '__CUSTOM_2', 'VALUE')`
- To insert an item at a specific position, pass the index `addToObject(obj, '__CUSTOM_2', 'VALUE', 4)`
