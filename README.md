This repo is created to easily create personal blogs under `yourgithubaccount.github.io/yourforkedrepo`.

- Fork this repository into your own repository (lets call it `yourforkedrepo`)
- Clone your forked repo to your computer

```console
$ git clone git@github.com:yourgithubaccount/yourforkedrepo.git
$ cd yourforkedrepo
$ git config user.name 'your name'; git config user.email 'your@email.domain'
$ git submodule update --init --depth 1
```

- Replace `Hugo-Test` in `title:` with your Blog's heading (eg: My Personal Blog) in this following file.

[config/_default/languages.en.toml](config/_default/languages.en.toml)

- replace `mohan43u.github.io/hugo-test` with your own url like `yourgithubaccount.github.io/yourforkedrepo` throughout this following file.

[.github/workflows/pages.yml](.github/workflows/pages.yml)

- remove following two files

[content/posts/2026/first.md](content/posts/2026/first.md)\
[content/posts/2026/second.md](content/posts/2026/second.md)

- Create your own content by running following commandline under cloned repository directory.

```
$ hugo new content content/posts/2026/first.md
```

- edit this `first.md` file in your favourite editor. once you conplete, then run the following commandline under cloned repository directory

```
$ git add content/posts/2026/first.md
$ git commit -m 'added first.md'
$ git push origin master
```

Thats all, wait for few seconds for github actions to deploy your blog, then your blog will appear at `https://yourgithubaccount.github.io/yourforkedrepo`.
