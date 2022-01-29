These templates describe how pages are generated.

* the homepage is `index.html`
* sections are `section.html`
* pages are `page.html`

`_index.md` files in the `/content/` folder define sections. Everything else is a page.

Sections can override the default template files.

Taxonomies are how Zola implements tagging and associative metadata. Other metadata goes in the `[extra]` section.

See the [Zola documentation](https://www.getzola.org/documentation/) and the [Tera documentation](https://tera.netlify.app/docs/) for more details.
