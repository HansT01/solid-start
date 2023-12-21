---
section: core-concepts
title: Route Pre-rendering
order: 5
---

# Route Pre-rendering

<table-of-contents></table-of-contents>

It can be beneficial to render pages at build time instead of on demand. We can accomplish this by passing
a prerender option to our SolidStart server. The simplest way to get started is pass a list of routes to be
pre-rendererd to the `routes` option.

```js
import { defineConfig } from "@solidjs/start/config";

export default defineConfig({
  start: {
    server: {
      prerender: {
        routes: ["/", "/about"]
      }
    }
  }
});
```

But what if we want to pre-render all of our pages? 
```js
import { defineConfig } from "@solidjs/start/config";

export default defineConfig({
  start: {
    server: {
      prerender: {
        crawlLinks: true
      }
    }
  }
});
```
For more information on prerender options, check out [Nitro's documentation](https://nitro.unjs.io/config#prerender)

