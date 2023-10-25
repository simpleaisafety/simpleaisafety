# Simple AI Safety

Source for [SimpleAISafety.org](https://simpleaisafety.org), a website that provides simple,
intuitive explanations for import AI (artificial intelligence) and AI safety concepts.


# Vision & Goals

We think that AI (artificial intelligence) has a lot of potential for doing
good but worry that risks are being neglected. One of the reasons for this is
the lack of easily accessible information both for laypeople and for people
with a technical background but not already deep into AIS (artificial
intelligence safety) topics. By easily accessible we mean two things:

* Appropriate given the reader's background knowledge
* In the reader's native language

To achieve this we want to present concepts that keep appearing in the
discussion around AI, ML (machine learning) and AIS in increasing levels of
complexity to cater to as many readers as possible. We also want to leverage
analogies, metaphors and drawings to serve as _intuition pumps_.

The three levels of complexity are:

* **Basic**: The target group is people with a high school degree or comparable
  general knowledge. A useful simplification, since we tend to overcomplicate,
  is to aim for: _Explain it to me like I am 5_. Even experts can frequently
  benefit from simplified explanations of new concepts because they are easier
  to remember and allow you to mentally start attaching other concepts to them,
  building up a more complex mental model over time. The writer should avoid
  technical jargon and math.
* **Intermediate**: The target group is people with a bachelor's degree in
  computer science, physics or some other technical subject. The writer should
  use technical jargon, code samples and math where appropriate.
* **Advanced**: The target group is people with a master's degree in AI/ML or
  job experience in AI/ML. The writer should probably limit themself to linking
  to third-party resources for now.

This project is meant to be collaborative. We kindly ask informed readers to
submit new content, corrections and other kinds of improvements. To do so you
can submit a pull request (see below), which requires some technical
background, write a bug report
(https://github.com/simpleaisafety/simpleaisafety/issues/new/choose) or send 
an e-mail to info@simpleaisafety.org


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
