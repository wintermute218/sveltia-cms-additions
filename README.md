# Sveltia CMS Additions on Cloudflare Workers

This repository deploys [Sveltia CMS Additions](https://github.com/sveltia/sveltia-cms-additions) to Cloudflare Workers. It only contains configuration: the code comes from the `@sveltia/cms-additions` npm package.

See the [setup guide](https://github.com/sveltia/sveltia-cms-additions/blob/main/docs/setup.md) for connecting the CMS and the first-run wizard.

## Updating

Dependabot opens a pull request when a new version is released. Merge it, and Workers Builds deploys the update. You can also change the version of `@sveltia/cms-additions` in `package.json` yourself.

Don’t change `wrangler.jsonc` unless the release notes ask you to. The one exception is `name`, before the first deploy, when you deploy more than one copy to the same Cloudflare account: two Workers with the same name are one Worker. To serve several sites, you can also use [tenants](https://github.com/sveltia/sveltia-cms-additions/blob/main/docs/setup.md#several-sites-on-one-worker) in a single Worker.
