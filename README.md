# Parametron landing page

This repository contains the public landing page for Parametron: a small static
site built with HTML, CSS, and local brand assets. It has no client-side
JavaScript, no runtime or client-side dependencies, and no application build
step. Deployment tooling may use Cloudflare Wrangler.

## Local preview

Website files live in `public/`. Open `public/index.html` in a browser, or serve
the site from the repository root with Python 3:

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory public
```

Then open <http://localhost:8000>.

## Deployment

The site is deployed as static assets from `public/`, configured in
`wrangler.jsonc`. Cloudflare Workers Builds can run `npx wrangler deploy`.
No application build step is required.

### Continuous deployment

Pull requests receive Cloudflare preview deployments for visual verification.
After a pull request is merged to `main`, Cloudflare automatically deploys the
site to production through the repository's GitHub integration.

## Public project

- [Parametron on GitHub](https://github.com/parametron-io/)
- [Public engineering documentation](https://github.com/parametron-io/parametron-docs)

## Licensing

Website source code is licensed under the [MIT License](LICENSE).

The Parametron name, wordmark, logo, favicons, and other brand assets are not
licensed under MIT. Reuse of the source code does not grant rights to use
Parametron names or marks.
