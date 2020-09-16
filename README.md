# Svelte App With Global SCSS Support

This is a [Svelte](https://svelte.dev) template that features global SCSS support by utilizing [svelte-preprocess](https://github.com/sveltejs/svelte-preprocess).

You can create a new project based on this template using [degit](https://github.com/Rich-Harris/degit)

```bash
npx degit sensanaty/svelte-scss-template svelte-app
cd svelte-app
```

## Getting started

Install the project dependencies

```bash
npm install
```

or

```bash
yarn install
```

Then, to start the [Rollup](https://rollupjs.org) dev server

```bash
npm run dev
```

or 

```bash
yarn dev
```

Navigate to [localhost:5000](http://localhost:5000). You should see the app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

## Global SCSS Variables

By default, this template will prepend the `/src/assets/styles/global.scss` file everywhere where `scss` is being used. Note that `prependData` only works with a string, as such there can only be one file imported. The best solution for multiple files would be to create separate`scss` files, and to import them all into the `global.scss` file.

Another thing to keep in mind, to apply global styles for generic `HTML` elements like the `body` element for example, you have to use the `:global()` magic selector. Read more about styling in Svelte [here](https://svelte.dev/docs#style).

## Building and running in production mode

To create an optimised version of the app:

```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

## Using TypeScript

This template comes with a script to set up a TypeScript development environment, you can run it immediately after cloning the template with:

```bash
node scripts/setupTypeScript.js
```

Or remove the script via:

```bash
rm scripts/setupTypeScript.js
```

## Deploying to the web

### With [Vercel](https://vercel.com)

Install `vercel` if you haven't already:

```bash
npm install -g vercel
```

Then, from within your project folder:

```bash
cd public
vercel deploy --name my-project
```

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
