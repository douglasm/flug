# flug
The Hugo version of the FLUG site.

To change it, first you need to install [Hugo](https://gohugo.io/).

Hugo is a static site generator written in Go, which means the Hugo app has no dependencies, you just install the executable.

Once Hugo is installed navigate to the directory containing this repository and edit the relevant files. Most of the files are called <filename>.md and are in the content/ directory. They are formatted in Markdown. The only HTML page is index.html which is in the layouts/ directory.

### To test your content

run hugo server --theme=flug

This will start a server which you can access through [http://127.0.0.1:1313/](http://127.0.0.1:1313/).

### To build a deployable version
run hugo 

This will create the files for the static site in public/ the contents of it are deployed to the site.