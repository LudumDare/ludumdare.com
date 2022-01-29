# The Ludum Dare resources section
The resources section collects information that is useful to participants of Ludum Dare events. This section is further broken down into the following subsections. 

* [Rules](rules) - The Rules for Ludum Dare events
* [Best Practices](best-practices) - Non-rule recommendations for participants
* The Knowledge Base
  * [Questions](questions) - Frequently asked questions
  * [Topics](topics) - Further details on topics raised by questions, the Rules, and Best Practices

See sections for more details.

**IMPORTANT**: The knowledge base should only contain articles about the Ludum Dare event and it's websites. Articles on game jamming and making games should go elsewhere, such as the [Jammer Academy](https://github.com/JammerAcademy).


# Knowledge Base Author's Guide
To contribute an article (answers or topics), you should fork the `ludumdare.com` repository, and submit it as a pull request. See the editor's guide for how to get started (TODO).

Most knowledge base articles will be **Questions** (with answers). Questions should aim to be short and brief. Some questions may require explaining terms or concepts. For the times when linking Wikipedia just wont do, we have Topics.

**Topics** are articles that expand on a topic in detail. Their role is similar to a wiki or encyclopedia. Topics should add value, such as calling out nuances specific to us, or by providing a summary where Wikipedia might be overwhelming.


## How to add articles
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


## Additional advice
Topics shouldn't be orphaned. Questions, other topics, the Rules, and the Best Practices guide should make reference to every topic somewhere.
