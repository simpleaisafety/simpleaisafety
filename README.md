# Simple AI Safety

Source for [SimpleAISafety.org](https://simpleaisafety.org), a website that provides simple,
intuitive explanations for import AI (artificial intelligence) and AI safety concepts.


## How to contribute

### Setup

* [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  * Why? Git is used to download the website content and then later upload your
    modifications.
* [Install Hugo](https://gohugo.io/installation/) (**extended version**)
  * Why? Hugo is a static site generator. It is used to convert text files (in
    markdown format) to a regular HTML website.
* Use some Git tool (e.g. Git Bash) and go the the directory on your PC where
  you would like to save the project.
* Get the project e.g. by executing `git clone
  git@github.com:simpleaisafety/simpleaisafety.git`
* Inside the project directory use a terminal/console to execute `hugo server`.
* Access the website preview with http://localhost:1313

### Make changes

To modify an existing page edit anything in the `content/` directory.

To create a new page execute something like `hugo new "posts/my-new-concept.md"`

Contribute your modification back to the main project via a pull request e.g. as documented
[here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)


## Theme

The theme is the overall look and feel of the website. We are currently using a
third-party theme. You can probably ignore this section.

```bash
git remote add -f theme-meme https://github.com/reuixiy/hugo-theme-meme
git subtree add --prefix themes/meme theme-meme master --squash
```

Update later

```bash
git fetch theme-meme master
git subtree pull --prefix themes/meme theme-meme master --squash
```


## Design decisions

### Static site generator

Why are you using a static site generator instead of a CMS or a custom-written
web application? Because it is easier to set up, requires essentially no
maintenance (as opposed to a CMS that needs to be updated), requires no user
management (GitHub does it for you) and is free (minimal compute needed, no DB
needed). This decision comes with some disadvantages so it might be changed in
the future. e.g. you can do no dynamic processing on the server (possibly
particularly limiting where search is concerned) end and asking people to make
contributions via GitHub might be too big a hurdle.

It is possible to build a dynamic frontend application (e.g. React) on top of
the static site.
