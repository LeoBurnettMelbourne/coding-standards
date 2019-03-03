# coding-standards
Guidelines that should be adhered to when writing code. Consistent code is easier to read and leads to less bugs. 

## Text editor/IDE

* Use [EditorConfig](http://editorconfig.org/) standard settings
* Install the following packages so we code consistently:
   - Atom: [TBC]
   - VSCode: `code --install-extension dbaeumer.vscode-eslint  --install-extension shinnn.stylelint --install-extension aaron-bond.better-comments --install-extension EditorConfig.EditorConfig --install-extension esbenp.prettier-vscode`

## Naming conventions
* For most files, use dashes: `file-name-1.jpg`.
* Javascript-like files and modules, use camel-case: `moduleNo1.js`.
* AEM components, use camel-case:

```
// AEM component
moduleNo1

// AEM component associated files
moduleNo1.js
moduleNo1.css

// AEM component front-end sub-modules use dashes
moduleNo1-user-notification.js
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
* Format: use [Stylelint](https://github.com/stylelint/stylelint) standard config and [Prettier](https://prettier.io/)
* Units: use REMs for font-size and layouts, EMs are also acceptable. Avoid pixels so that layouts can be scaled up and down 

## Javascript
* Latest ECMAScript spec (transpiled)
* No jQuery
* Use [Airbnb styleguide](http://github.com/airbnb/javascript)
* When selecting DOM elements, use data attribute selectors, e.g. `this.element.querySelector('[data-component-name-selector-name]')`
* Lint with [Prettier](https://prettier.io/) and [ESLint](https://eslint.org/)
* Write [JSDoc](http://usejsdoc.org/) comments

## Tracking / analytics
* Only track elements using `tracking` data attribute selectors, e.g. `document.querySelector('[data-tracking-selector-name]')`

## Version control
* Commit message format `[componentName] - JIRA ticket number (if relevant) - description of change`. E.g. `[headerComponent] - HODSO-401 - Fix bug with icon width in Safari 10`
* Review changes using `diff` before committing
* Feature-branches and pull-requests recommended

## README.md
* Include in root of every project with the following:
     * Front-end setup (e.g. `npm install`)
     * Front-end development (e.g. `npm start`)
     * Backend setup/server (no sensitive information)
     * Deployment process / server environments
     * Browser support

