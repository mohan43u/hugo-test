This repo is created to easily create personal blogs under `yourgithubaccount.github.io/yourforkedrepo`.

- Fork this repository into your own repository (lets call it `yourforkedrepo`)
- Go to repository `Settings -> Pages`, under `Build and Deployment` change `Source` to `Github actions`.
- Clone your forked repo to your computer

```console
$ git clone git@github.com:yourgithubaccount/yourforkedrepo.git
$ cd yourforkedrepo
$ git config user.name 'your name'; git config user.email 'your@email.domain'
$ git submodule update --init --depth 1
```

- Replace `Hugo-Test` in `title:` with your Blog's heading (eg: My Personal Blog) in this following file.

[config/_default/languages.en.toml](config/_default/languages.en.toml)

- Replace `mohan43u.github.io/hugo-test` with your own url like `yourgithubaccount.github.io/yourforkedrepo` throughout this following file.

[.github/workflows/pages.yml](.github/workflows/pages.yml)

- Create your own content by creating `.md` files under `content/posts/2026/` directory like `content/posts/2026/first.md`
- Make sure your `.md` files begin with following header (modify the `date` and `title` as you wish)
```
+++
date = '2026-07-14T19:29:00Z'
title = 'my blog post'
+++
```

- Once you conplete your blog post, run the following commandlines to add your blog post (replace `first.md` with your `.md` filename)

```
$ git add content/posts/2026/first.md
$ git commit -m 'added first.md'
$ git push origin master
```

Thats all, wait for few seconds for github actions to deploy your blog, then your blog will appear at `https://yourgithubaccount.github.io/yourforkedrepo`. You can redesign your blog by reading the documents of `blowfish` from here [https://blowfish.page/docs/](https://blowfish.page/docs/).
