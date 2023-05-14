---
title: Group Array of Objects by Key
category: Frontend Cheetseat
date: 2021-10-05
tags: ['array', 'JavaScript']
author: Suresh Kumar Mukhiya
thumbnailText: 'Group array of objects'
---

### Problem:

Given an arry of objects, we need to group objects by any key.

### Input:

```json
const arrayObjects = [
   {
      "Phase":"Phase 1",
      "Step":"Step 1",
      "Task":"Task 1",
      "Value":"5"
   },
   {
      "Phase":"Phase 1",
      "Step":"Step 1",
      "Task":"Task 2",
      "Value":"10"
   },
   {
      "Phase":"Phase 1",
      "Step":"Step 2",
      "Task":"Task 1",
      "Value":"15"
   },
   {
      "Phase":"Phase 1",
      "Step":"Step 2",
      "Task":"Task 2",
      "Value":"20"
   },
   {
      "Phase":"Phase 2",
      "Step":"Step 1",
      "Task":"Task 1",
      "Value":"25"
   },
   {
      "Phase":"Phase 2",
      "Step":"Step 1",
      "Task":"Task 2",
      "Value":"30"
   },
   {
      "Phase":"Phase 2",
      "Step":"Step 2",
      "Task":"Task 1",
      "Value":"35"
   },
   {
      "Phase":"Phase 2",
      "Step":"Step 2",
      "Task":"Task 2",
      "Value":"40"
   }
];
```

### Expected Output:

```json
{
  "Task 1": [
    {
      "Phase": "Phase 1",
      "Step": "Step 1",
      "Task": "Task 1",
      "Value": "5"
    },
    {
      "Phase": "Phase 1",
      "Step": "Step 2",
      "Task": "Task 1",
      "Value": "15"
    },
    {
      "Phase": "Phase 2",
      "Step": "Step 1",
      "Task": "Task 1",
      "Value": "25"
    },
    {
      "Phase": "Phase 2",
      "Step": "Step 2",
      "Task": "Task 1",
      "Value": "35"
    }
  ],
  "Task 2": [
    {
      "Phase": "Phase 1",
      "Step": "Step 1",
      "Task": "Task 2",
      "Value": "10"
    },
    {
      "Phase": "Phase 1",
      "Step": "Step 2",
      "Task": "Task 2",
      "Value": "20"
    },
    {
      "Phase": "Phase 2",
      "Step": "Step 1",
      "Task": "Task 2",
      "Value": "30"
    },
    {
      "Phase": "Phase 2",
      "Step": "Step 2",
      "Task": "Task 2",
      "Value": "40"
    }
  ]
}
```

### Solution:

```javascript
const groupBy = (items, key) =>
  items.reduce(
    (result, item) => ({
      ...result,
      [item[key]]: [...(result[item[key]] || []), item]
    }),
    {}
  )
```
