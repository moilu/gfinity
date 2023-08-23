# gfinity

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out the [documentation](https://nuxtjs.org).

## Thought process

1.- Create the Home component, I knew that I would need this for the main
2.- Second I create the navigation bar. At the moment of creating I put it inside the home component.
3.- Then I create fake data to focus on the layout of the table
4.- After stying was finished I started to read the sanity docs to be able to query for the table content.
5.- I installed de sanity dependency following the docs info and create the sanity file to initialize the client.
6.- I imported the client into the table content file and started to make calls to sanity to fetch information.
7.- Used the sanity response information to replace fake data.
8.- Create default layout to put navigation in it. This would help so it can be visible on all pages.
