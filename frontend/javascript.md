# JavaScript style guide

This document outlines the way we write JavaScript. It's a living guide, growing the same way our practices do.

Client-side JavaScript architecture
-----------------------------------

### Type declaration

**TODO: add code snippets** 

Make use of `type` declarations over `interface`.

Component `props` should be not be typed inline in the component.

### Component imports

Only import what is needed.

Do this:

```js
import { flatten, merge } from 'lodash';
```
_Don't_ do this:

```js
import * from 'lodash';
```

**TODO:** 

- Import order
- Import separation
- Import with "@"

### Directory structure

- Keep each component in its folder by creating a root folder with its name and add related files inside it.
- No component folder nesting (See frontend/src/chat/components)
- PascalCase for the component folder name and component files
- Append "Dialog" to the end of the component name
- Anything other than the components should use the kebab-case.

**TODO: add mention of this in css guide page**
Styles:
- Component styles should be kept in a separate file and imported via the useStyles hook.
- Very common styles should reside in a separate common styles folder

### Mutations

Do not use mutations directly inside components, they should be imported from associated store.

### Links

Use custom link component from "@/common/components/Link", that takes into account localized route names

### Exports

Use named exports instead of default exports

**TODO** Add "Component architecture" section and group some of the above
