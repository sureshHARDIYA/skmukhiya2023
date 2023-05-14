---
title: Concatenate array of objects inside an array of objects
category: Frontend Cheetseat
date: 2021-10-26
tags: ['array', 'JavaScript']
author: Suresh Kumar Mukhiya
thumbnailText: 'Concatenate array of objects'
---

### Problem:

Given an array of objects, we want to concatenate nested array of objects. Look at the example objects given below.

### Input:

```javascript
const data = {
  activePolicies: [
    {
      policy: 1,
      locations: [
        {
          address: 'address1',
          locationID: 1
        },
        {
          address: 'address2',
          locationID: 2
        }
      ]
    },
    {
      policy: 2,
      locations: [
        {
          address: 'address3',
          locationID: 3
        },
        {
          address: 'address4',
          locationID: 4
        }
      ]
    }
  ],
  inActivePolicies: [
    {
      policy: 3,
      locations: [
        {
          address: 'address5',
          locationID: 5
        },
        {
          address: 'address6',
          locationID: 6
        }
      ]
    },
    {
      policy: 4,
      locations: [
        {
          address: 'address7',
          locationID: 7
        },
        {
          address: 'address8',
          locationID: 8
        }
      ]
    }
  ]
}
```

### Expected Output:

```javascript
const results = [
  {
    address: 'address1',
    locationID: 1
  },
  {
    address: 'address2',
    locationID: 2
  },
  {
    address: 'address3',
    locationID: 3
  },
  {
    address: 'address4',
    locationID: 4
  },
  {
    address: 'address5',
    locationID: 5
  },
  {
    address: 'address6',
    locationID: 6
  },
  {
    address: 'address7',
    locationID: 7
  },
  {
    address: 'address8',
    locationID: 8
  }
]
```

### Solution 1:

```javascript
function method1() {
  const policies = _.concat(data.inActivePolicies, data.activePolicies)

  const results = _.reduce(
    policies,
    (acc, item) => {
      return _.concat(acc, item.locations)
    },
    []
  )

  return results
}
```

### Solution 2: (Fastest solution)

I have created a benchmark here to test the fastest solution. [Hope the solution is still active when you are reading the blog.](https://jsbench.me/aukv7zsr0t/1)

```javascript
function method2() {
  let newArray = []

  data.activePolicies.forEach(item => {
    item.locations.forEach(loc => {
      newArray.push(loc)
    })
  })

  data.inActivePolicies.forEach(item => {
    item.locations.forEach(loc => {
      newArray.push(loc)
    })
  })

  return newArray
}
```

### Solution 3:

```javascript
function method3() {
  let newArray = []

  for (const inAct of data.activePolicies) {
    for (const inActInner of inAct.locations) {
      newArray.push(inActInner)
    }
  }

  for (const inAct of data.inActivePolicies) {
    for (const inActInner of inAct.locations) {
      newArray.push(inActInner)
    }
  }

  return newArray
}
```
