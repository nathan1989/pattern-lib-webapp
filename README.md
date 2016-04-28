# AC pattern library

## Setup

Run `npm install && bower install` to get the dev dependencies and third party libraries.

## Build & development

Run `gulp` for building and `gulp serve` for preview.

Run `bower install --save <package>` to install frontend dependencies.

## Creating a new page

To create a new 'page', add a `.njk` file to app/pages. Add the following templating code to the new page:

`{% block title %}` Title of your page goes here `{% endblock %}`

`{% extends "layouts/default.njk" %}`

`{% set active_page = '` No spaces, hyphens only variable name for the page  `' %}`

`{% block content %}`
	Add your HTML code here
`{% endblock %}`

In the sidebar navigation in `app/layouts/default.njk`, add the new nav item for the new page as follows:

```html
<li><a href="new-page.html" class="{%if active_page == 'new-page' %} active {% endif %}">New Page</a></li>
```