# Yunpeng's Blog

This repository is meant for [Yunpeng](https://yunpengn.github.io/)'s personal blog website. It is proudly powered by [Hexo.js](https://hexo.io/).

## Why I choose Hexo.js

- The front-end styling should be reasonably consistent and polished. For a developer like me who is better at backend programming, it is difficult to start front-end design from scratch. Thus, I have to choose a framework, or a website generator.
- I want a blog website that only consists of static webpages. This provides me with more options to host it. For instance, [GitHub Pages](https://pages.github.com/) certainly only supports static webpages. Thus, I cannot use any content management system (CMS) with dynamic pages, like [WordPress](https://wordpress.org/) and [Drupal](https://www.drupal.org/).
- I want to use a Windows-based development machine. This means some programming languages like Ruby may be troublesome. Thus, I will not choose engines like [Jekyll](https://jekyllrb.com/).

Given all the factors mentioned above, I choose [Hexo.js](https://hexo.io/) in the end.

## Development Setup

- Make sure you have installed [Node.js](https://nodejs.org/), [Npm]() and [Git](https://git-scm.com/) on your development machine. Npm should come with Node.js.
	- You chould check by `git --version`, `node -v` and `npm -v`.
- Install the command line interface of [Hexo.js](https://hexo.io/) (recommended using npm).
```bash
npm install hexo-cli -g
```
- Fork and clone this repository to your computer.
```bash
git clone git@github.com:yunpengn/blog.git
```
- Navigate to this directory.
```bash
cd blog
```
- Install all the dependencies stated in `package.json` (or `package-lock.json`).
```bash
npm install
```
- Run the Hexo server to host the website locally.
```bash
hexo server
```
- Now, you can visit the website at `http://localhost:4000/blog/`

## Deployment

_Notice: we are using [GitHub Pages](https://pages.github.com/) to deploy the website. For other deployment approaches, see the official [documentation](https://hexo.io/docs/deployment.html) for more information._

- Make sure you have declared the required dependency in `package.json`. For instance, if you need to deploy to a Git repository, run the following command
```shell
npm install hexo-deployer-git --save
```
- Check the settings in `_config.yml` is correct:
```yaml
deploy:
  type: git
  repo: <The URL to your Git repository>
  branch: <The branch for deployment>
  message: <The commit message>
```
- Deploy the website by running the following commands:
```shell
# Clean the database and the public folder
hexo clean
# Generate all the static webpages
hexo generate
# Deploy the website
hexo deploy
```
- _Notice: You should have access to the Git repository for deployment._

## Acknowledgements

The theme used by this blog website benefits from [Aath](https://github.com/lewis-geek/hexo-theme-Aath). I would personally appreciate [Lewis](http://lewis.suclub.cn/)'s awesome work. 

## Licence

[GNU General Public Licence 3.0](LICENSE)
