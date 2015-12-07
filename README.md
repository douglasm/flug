# flug
The Hugo version of the FLUG site.

To change it, first you need to install [Hugo](https://gohugo.io/).

Hugo is a static site generator written in Go, which means the Hugo app has no dependencies, you just install the executable.

Once Hugo is installed navigate to the directory containing this repository and edit the relevant files. Most of the files are called <filename>.md and are in the content/ directory. They are formatted in Markdown. The only HTML page is index.html which is in the layouts/ directory.

### Local testing

`hugo server --theme=flug`

This will start a server which you can access through [http://127.0.0.1:1313/](http://127.0.0.1:1313/).

### To build a deployable version

There is a `generated` branch of this repo which contains the current static site. Switch to this branch

`git checkout generated`

Rebase the latest changes (this should never conflict, since this branch only holds code in /public/)

`git rebase master`

Generate the site into /public/ and squash into the top commit

```
hugo --theme=flug
git add -A
git commit --amend -m "Generate static site"
git push openshift HEAD:master -f
```

It's ok to squash the history here as the static site is always generated from the rest of the repo. This way the master branch stays clean.
