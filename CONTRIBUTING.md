# Contributing

All contributions are welcome to the project, the curators try to review all PRs as quickly as possible. 
Yet, this is a volunteer run project, so please be patient with it. If you are planning on submitting bigger 
changes to the projects, please open a github issue first and talk to the team before submitting to make 
sure your work will be accepted.

We might reject any contribution without stating a reason, but especially if the contribution or 
contributor in question is not following the [code of conduct](./CODE_OF_CONDUCT.md) or doesn't follow the 
right procedure outlined below.


## Submitting Project News

You have an important announcement or latest news related to web development in rust and you'd like to share 
them with the wider audience of this website? GREAT, here is how you can do that:

Just create a new file in `content/news` - we recommend to use Markdown. Make sure you set the `title`, the
`date`, the `source` and add all appropriate `tags`. Once you are done, please submit all of that as a pull-request 
and we'll get right on it!

## Complaining about incorrect text

Please open a github issue if you feel that anything is represented or out of date. Keep in mind that the description 
of a package is directly pulled from crates.io and won't be changed here.

## Local Development

This project is hosted on github pages and uses the [Zola](https://www.getzola.org/). Zola is a static website 
compiler – it uses our data to generate a bunch of HTML pages. If you do not have zola yet, you can install it 
by using brew (`brew install zola`), snap (`snap install --edge zola`) or any other way 
[outlined on the official website](https://www.getzola.org/documentation/getting-started/installation/).

To compile the documents, run from the main directory

```bash
zola serve
```

Now open a browser on `http://localhost:1111` and you'll be able to see the homepage in its latest version. 
Any changes you make immediately rerender the websites after saving the file, you just need to refresh the 
browser.

To generate a production build, run:

```bash
zola build
```
