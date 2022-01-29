# Frequently Asked Questions and Knowledge Base authors guide
**IMPORTANT**: The knowledge base should only contain articles and frequently asked questions about the Ludum Dare event and website(s). How to make games, how to use specific tools, those should be added to the [Jammer Academy](https://github.com/JammerAcademy) as articles or as part of their knowledge base.


# Writer's Guide
todo


# How to add articles
Create a new `.md` file in the `/content/resources/questions/` or `/content/resources/topics/` folder.

File names should only contain lower case letters, numbers, and dashes. The article slug (URL) of the article will be the file name. For example, `how-to-upload.md` will get published at `ludumdare.com/resources/questions/how-to-upload/`.

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

As a rule of thumb, the title and filename of articles should match. For example, the filename for the above article should be `topic-or-question.md`.

Articles are sorted by weight. Articles without a weight will not show up on the directory pages (i.e. `/questions/` and `/topics/`). You should include a weight of `100` by default. Including a default will let us prioritize articles if we need to.

The `Categories` taxonomy let us categorize articles. You can include one or more categories each separated by commas. You can check [ludumdare.com/categories/](https://ludumdare.com/categories/) for a current list of categories. If you can't find an appropriate category, feel free to include a new one. Taxonomies automatically generate slugs (`Categories`->`categories`), so _do_ include capital letters and spaces where appropriate.

Be sure to include a blank line between the 2nd `+++` and the article text (notice the space in the example above). This isn't required by Zola, but it makes `.md` files more readable on GitHub. Omitting the blank line merges everything into a single paragraph.


### Articles with assets
If your article requires images or other files, create a folder instead.

Follow the same naming rules for `.md` files (lower case letters, numbers, and dashes). Create an `index.md` file, and any files you require inside the folder.

Check out [Derivative Works](topics/derivative-works/) for an example.
