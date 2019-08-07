## Gatsby Composer for Themes

### What is this?

A yarn workspaces composed space for developing, running and testing your Gatsby themes.

Based on [Composable yarn workspaces by @ChristopherBiscardi](https://www.christopherbiscardi.com/post/composing-yarn-workspaces) where you simply nest git repos that couldn't care less about each other :), and we've added a demo theme runner!

### Quick start

```
git clone git@github.com:demystifying-dev/gatsby-composer-for-themes.git my-dev-composer
cd my-dev-composer
yarn
```

Run demo on port 6209

yarn workspace demo develop -H 0.0.0.0 -p 6209

point browser at `http://myserver.org:6209/`

### Docs and Examples

Docs and more examples coming, but the basic idea is:

* Learn
    * Check out atomic commits to see how basic things are done step by step
* Playground
    * Using built-in yarn workspace theme plus built in runner
* Project workflow
    * Fork or clone
    * Invoke app repo in sub-directory as composed (own repo without using submodules) runner, replace in `package.json` as runner instead of `demo` (docs coming soon)
    * Invoke one or more themes as composed (own repo without using submodules) under themes directory, register as yarn workspaces in `package.json` and configure them in `gatsby-config.js`, etc.

In this way we can have a project by project monorepo with dependencies handled by yarn workspaces, plus easily re-usable themes without having to make them npm packages (which I would like to avoid as a day-to-day workflow).
