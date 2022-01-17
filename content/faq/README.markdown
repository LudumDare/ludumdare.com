# How to add topics and questions

Create a new '.md' file.

File names should only contain lower case letters, numbers, and dashes. The file name will be the same as the URL slug.

Front matter should include the following fields:

```
+++
title = "Topic or Question?"
weight = 100
+++
```

Frequently asked questions are sorted by weight. Topics without a weight will not show up on the `/faq/` page. You should include a weight of `100` by default. This ensures we can prioritize important topics ahead of others.


## Topics with assets
If your topic requires images or other files, you can alternatively create a folder.

Follow the same naming rules for your folder (lower case letters, numbers, and dashes). Create an `index.md` in the folder. Include any files you require inside the folder.

For an example, check out the [Derivative Works](derivative-works/) folder.
