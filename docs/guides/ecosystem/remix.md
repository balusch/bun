---
name: Build an app with Remix and Bun
---

{% callout %}
Remix currently relies on Node.js APIs that Bun does not yet implement. The guide below uses Bun to initialize a project and install dependencies, but it uses Node.js to run the dev server.
{% /callout %}

---

Initialize a Remix app with `create-remix`.

```sh
$ bunx create-remix

 remix   v1.19.3 💿 Let's build a better website...

   dir   Where should we create your new project?
         ./my-app

      ◼  Using basic template See https://remix.run/docs/pages/templates for more
      ✔  Template copied

   git   Initialize a new git repository?
         Yes

  deps   Install dependencies with bun?
         Yes

      ✔  Dependencies installed

      ✔  Git initialized

  done   That's it!

         Enter your project directory using cd ./my-app
         Check out README.md for development and deploy instructions.
```

---

To start the dev server, run `bun run dev` from the project root. This will start the dev server using the `remix dev` command. Note that Node.js will be used to run the dev server.

```sh
$ cd my-app
$ bun run dev
  $ remix dev

  💿  remix dev

  info  building...
  info  built (263ms)
  Remix App Server started at http://localhost:3000 (http://172.20.0.143:3000)
```

---

Open [http://localhost:3000](http://localhost:3000) to see the app. Any changes you make to `app/routes/_index.tsx` will be hot-reloaded in the browser.

{% image src="https://github.com/oven-sh/bun/assets/3084745/c26f1059-a5d4-4c0b-9a88-d9902472fd77" caption="Remix app running on localhost" /%}
