# Ludum Dare FAQ and Knowledge Base
yay

**NOTE:** The knowledge base should only contain articles and FAQ's about the Ludum Dare event and website(s). Generally questions about making games should go in the appropriate section of the [Jammer Academy](https://jammer.academy) knowledge base. In cases where it is tool _and_ Ludum Dare specific, it can be included here.


# How to add new articles
Create a new `.md` file in the `/content/faq/` folder.

File names should only contain lower case letters, numbers, and dashes. The article slug (URL) of the article will be the file name. For example, `best-practices.md` will get published at `ludumdare.com/faq/best-practices/`.

A simple article should be structured as follows.

```
+++
title = "Topic or question?"
weight = 100
[taxonomies]
Categories = ["Rules"]
+++

Answer to the topic or question.
```

As a rule of thumb, the title and the filename should match. For example, the filename for the above article should be `topic-or-question.md`.

FAQ articles are sorted by weight. Articles without a weight will not show up on the `/faq/` page. You should include a weight of `100` by default. Including the default ensures we can easily prioritize important topics ahead of others in the future.

The `Categories` taxonomy let us categorize articles. You can include one or more categories each separated by commas. You can check [ludumdare.com/categories/](https://ludumdare.com/categories/) for a current list of categories. If you can't find an appropriate category, feel free to include a new one. Taxonomies automatically generate slugs (`Categories`->`categories`), so _do_ include capital letters and spaces where appropriate.

Be sure to include a blank line between the 2nd `+++` and the article text. This isn't required by Zola, but it makes `.md` files more readable on GitHub. Omitting the blank line merges everything into a single paragraph.


## Articles with assets
If your article requires images or other files, you can alternatively create a folder.

Follow the same naming rules for `.md` files for your folder (lower case letters, numbers, and dashes). Create an `index.md` file, and any files you require inside the folder.

Check out the [Derivative Works](derivative-works/) for an example.
