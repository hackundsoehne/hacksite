# Hacksite

[![Netlify Status](https://api.netlify.com/api/v1/badges/27251695-05a8-41e9-8dde-1d8a1ad00193/deploy-status)](https://app.netlify.com/sites/elastic-jackson-156fc6/deploys)

This is the source code of the [HUGO](https://gohugo.io/) based Hack & Söhne organisation website. The website is deployed from this repository via [netlify](https://www.netlify.com/). **Note** that changes are published live from the `main` branch.

## Development

1. [Install HUGO](https://gohugo.io/getting-started/installing)
2. `git clone --recurse-submodules git@github.com:hackundsoehne/hacksite.git`
3. `cd hacksite`
4. `hugo server`

## Theme

This website uses the [Hackurat](https://github.com/hackundsoehne/hackurat) HUGO theme. It's managed via git submodules. To update the Hackurat theme submodule, run the following command and commit the resulting changes:

```sh
git submodule update --remote --merge
```