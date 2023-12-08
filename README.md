### Init hexo project

```shell
sudo npm install -g hexo-cli
hexo init hatsuka05 && cd hatsuka05
npm install
hexo server
```

### Gitignore file

```
.DS_Store
yarn.lock
package-lock.json
db.json
Thumbs.db
_multiconfig.yml
*.log
node_modules/
public/
.deploy*/
```

### Create new post, draft, page

```shell
hexo new [type] [title]
hexo new post post1
hexo new draft draft1
hexo new page page1
```

### Show list page, post, route, tag, category

```shell
hexo list [type]
```

### Deploy

Update ==\_config.yml== file

```
deploy:
  type: git
  branch: gh-pages <== github page branch
  repo: git@github.com:***repo***.git <== if using ssh
  # repo: https://oauth2:GITHUB_TOKEN_HERE@github.com/***repo***.github.io  <== if using oauth2
  # repo: https://github.com/***repo***.github.io <== if not using oauth2 and not using ssh
```

\*note: if you are using custom domain for github page, make sure CNAME file is copied to ==public/== folder

Deploy site

```shell
hexo clean && hexo deploy
```
