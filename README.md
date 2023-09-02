# Simple AI Safety

Website https://simpleaisafety.org


## How to contribute

* [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Install Hugo](https://gohugo.io/installation/)
* Use some Git tool (e.g. Git Bash) and go the the directory on your PC where you want to save the project.
* Get the project e.g. by executing `git clone git@github.com:simpleaisafety/simpleaisafety.git`
* Inside the project directory use a terminal/console to execute `hugo server`
* Access the website with http://localhost:1313
* Make changes via PR (pull requests) e.g. a documented [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)


## Theme

```bash
git remote add -f theme-meme https://github.com/reuixiy/hugo-theme-meme
git subtree add --prefix themes/meme theme-meme master --squash
```

Update later

```bash
git fetch theme-meme master
git subtree pull --prefix themes/meme theme-meme master --squash
```
