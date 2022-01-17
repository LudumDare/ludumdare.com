# How to add new FAQ articles
Create a new `.md` file in the `/content/faq/` folder.

File names should only contain lower case letters, numbers, and dashes. The article slug (URL) of will be the file name. For example, `best-practices.md` will get published at `ludumdare.com/faq/best-practices/`.

A simple article should be structured as follows.

```
+++
title = "Topic or Question?"
weight = 100
+++

Answer to the topic or question.
```

FAQ articles are sorted by weight. Articles without a weight will not show up on the `/faq/` page. You should include a weight of `100` by default. Including the default ensures we can easily prioritize important topics ahead of others in the future.

Be sure to include a blank line between the 2nd `+++` and the article text. This isn't required by Zola, but it makes `.md` files more readable on GitHub. Omitting the blank line merges everything into a single paragraph.


## Articles with assets
If your article requires images or other files, you can alternatively create a folder.

Follow the same naming rules for `.md` files for your folder (lower case letters, numbers, and dashes). Create an `index.md` file, and any files you require inside the folder.

Check out the [Derivative Works](derivative-works/) for an example.
