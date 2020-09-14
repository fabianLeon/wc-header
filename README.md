## WebComponent header simple with svelte and use angular app

1. Install

```bash
npm i wc-header
```

in angular.json add into scripts

```bash
 "scripts": [
    ...
    "node_modules/wc-header/public/build/bundle.js"
    ...
    ]
```
2. In app.module

```typescript
import { NgModule, CUSTOM_ELEMENTS_SCHEMA } from '@angular/core';

...

@NgModule({
  ...
  schemas: [ CUSTOM_ELEMENTS_SCHEMA ]
})
```
3. Use into html. 
```html
<svelte-beauty-header 
    name="Title application"
    subname="Subtitle application"
    description="Description ... "
    button="Label Button"
    active="true">
</svelte-beauty-header>
```