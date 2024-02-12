# hono-jsx

Fork of [`hono/jsx` runtime exports](https://github.com/honojs/hono/blob/main/package.json#L122-L136) with direct import support.

> **What is "direct import support"?**
>
> In the [`hono`](https://github.com/honojs/hono) package, the `hono/jsx/*` entrypoints are exposed via [`package.json#exports`](https://github.com/honojs/hono/blob/main/package.json#L122-L136). Unfortunately, some runtimes & bundlers (most notably Vercel Edge Functions) have [poor support for `package.json#exports`](https://github.com/honojs/middleware/issues/333#issuecomment-1938293091). This fork exposes the `hono/jsx/*` entrypoints **directly** in the `hono-jsx` package, so that they can be imported without relying on `package.json#exports`.