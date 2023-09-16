# Webpack magic comments

Inline comments to make features work. By adding comments to the import, we can do things such as name our chunk or select different modes. For a full list of these magic comments see the code below followed by an explanation of what these comments do.

```javascript
// Single target
import(
  /* webpackChunkName: "my-chunk-name" */
  /* webpackMode: "lazy" */
  /* webpackExports: ["default", "named"] */
  /* webpackFetchPriority: "high" */
  'module'
);

// Multiple possible targets
import(
  /* webpackInclude: /\.json$/ */
  /* webpackExclude: /\.noimport\.json$/ */
  /* webpackChunkName: "my-chunk-name" */
  /* webpackMode: "lazy" */
  /* webpackPrefetch: true */
  /* webpackPreload: true */
  `./locale/${language}`
);
```

### webpackPrefetch

```javascript
import(/* webpackPrefetch: true */ './some-module.js');
```

When webpack sees this comment, it adds this to your document's head:

```javascript
<link rel="prefetch" as="script" href="/static/js/1.chunk.js">
```

With this, the browser will automatically load this JavaScript file into the browser cache so it's ready ahead of time.

[Full Sourse](https://webpack.js.org/api/module-methods/#magic-comments)
