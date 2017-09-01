# coding-standards
Guidelines that should be adhered to when writing code. Consistent code is easier to read and leads to less bugs. 

## Text editor/IDE

* Use [EditorConfig](http://editorconfig.org/) standard settings
* When using Atom, install the following packages so we code consistently: `apm install linter linter-eslint linter-tslint linter-stylelint linter-tidy atom-typescript`
* The following Atom packages are recommended, but optional `apm install file-icons emmet pigments terminal-plus`

## Naming conventions
* For most files, use dashes: `file-name-1.jpg`.
* Javascript-like files and modules, use camel-case: `moduleNo1.js`.
* AEM components, use camel-case:

```
// AEM component
moduleNo1

// AEM component associated files
moduleNo1.ts
moduleNo1.css

// AEM component front-end sub-modules use dashes
moduleNo1-user-notification.ts
moduleNo1-user-notification.css

// AEM component with BEM syntax for styles
.moduleNo1__heading,
.moduleNo1__heading--large
```

## HTML
* Be sure to [validate](https://validator.w3.org/)
* Adhere to [HTML5 sections and outlines](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML_sections_and_outlines) (for accessibility) and [validate](https://gsnedders.html5.org/outliner/)

## Styles
* BEM syntax, use [ampersand selector to nest styles](https://jonsuh.com/blog/sass-bem-selector-and-trailing-ampersand/#bem-selector-support)
* Format: use Stylelint standard config
* Units: use REMs for font-size and layouts, EMs are also acceptable. Avoid pixels so that layouts can be scaled up and down 

## Javascript
* ES6 Typescript
* No jQuery
* Use [Airbnb styleguide](http://github.com/airbnb/javascript)
* When selecting DOM elements, use data attribute selectors, e.g. `this.element.querySelector('[data-component-name-selector-name]')`

## Tracking / analytics
* Only track elements using `tracking` data attribute selectors, e.g. `document.querySelector('[data-tracking-selector-name]')`

## Version control
* Commit message format `[component] - JIRA ticket number (if relevant) - description of change`. E.g. `[header] - HODSO-401 - Fix bug with icon width in Safari 10`
* Review changes using `diff` before committing

## README.md
* Include in root of every project with the following:
     * Job code
     * Team members (inc producers, designers)
     * Front-end setup (e.g. `yarn install`)
     * Front-end development (e.g. `yarn start`)
     * Backend setup/server (no sensitive information)
     * Browser support

