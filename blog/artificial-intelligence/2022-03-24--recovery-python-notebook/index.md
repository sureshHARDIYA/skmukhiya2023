---
title: 'Recovering deleted iPython Notebooks cells'
date: 2022-03-24
category: Artificial Intelligence
tags: ['Notebook', 'Python', 'iPython']
author: Suresh Kumar Mukhiya
thumbnailText: 'Recovering deleted iPython Notebooks'
---

Life is full of surprises!

Something intresting happened to me yesterday with my work computer. I worked on a Python script to batch import data from two excel files, merge them, and send POST requests to multiple `REST` endpoints.

I had it working. I saved the file. As usual, after 4, I went home. The computer was in sleep mode. The following day, I found out that the Python notebook had crashed. I restarted the notebooks, and I was surprised to find out none of the code I did yesterday persisted in the notebook.

Seriously! It appeared to me that yesterday was missing from my month. I could have recoded as it was fresh in my brain, but I tried to find out if I could recover the code.

So, I did what everyone would have done.
I checked if a version of the notebook is saved. Nope!

I checked if the notebook had checkpoints saved. Nope!

Desperate enough, I even tried to press `CTRL + Z`, thinking some magic might happen.

I googled!

- Some blogs said if the file is deleted, try the cache version like `~/.cache/chromium/Default/Cache/` and then use the `grep` command to find keywords in your code. I tried, did not work.
- Some blogs and StackOverflow mentioned checking `Trash` if it is deleted.

I tried several other options. None of them worked. Then I found an answer where I could save all my IPython history to a file. And Bingo! The command saved my day.

```javascript
%history -g -f anyfilename
```

Just execute the command in a cell in your notebook. The command writes all the history to a file named `anyfilename`.

And there you go.

Happy Recovery !!
