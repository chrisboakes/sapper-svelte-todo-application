# A simple Sapper/Svelte TODO application

Built for [this tutorial](https://chrisboakes.com/getting-started-with-sapper-and-svelte/).

## Running the project

Install the dependencies and run the project:

```bash
npm install # or yarn
npm run dev
```

You should see the project running on [localhost:3000](http://localhost:3000).

## Static rendering

Run:

```bash
npm run export
```

Your compiled project will now sit in `__sapper__/export`.

## Deploying to Netlify

If you'd like to host your static build on Netlify, it's extremely simple:

- Log in to your [Netlify](https://www.netlify.com/) account
- Create a new site from Git and select your repository
- Select your branch
- Set the build command as `npm run export`
- Set the publish directory as `__sapper__/export`
