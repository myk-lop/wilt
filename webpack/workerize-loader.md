# workerize-loader

A webpack loader that moves a module and its dependencies into a Web Worker, automatically reflecting exported functions as asynchronous proxies.

- Bundles a tiny, purpose-built RPC implementation into your app
- If exported module methods are already async, signature is unchanged
- Supports synchronous and asynchronous worker functions
- Works beautifully with async/await
- Imported value is instantiable, just a decorated Worker

[Source (npm package)](https://www.npmjs.com/package/workerize-loader)
