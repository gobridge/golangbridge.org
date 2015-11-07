# How to contribute

Note: Maintainers of this repository have [additional instructions for maintainers](#maintainers) on how to deploy the generated files to github pages.

----------
The GoBridge website contains information for people interested in learning about what we do and who we are, our scheduled events, how to contact us, etc.

As with all of our resources, this is a community driven work by volunteers and for volunteers who benefit from GoBridge. This means YOU! If you are interested in improving the UX and/or design of the website, we encourage you to do so and hope to make your process of contributing as easy as possible with the detailed step-by-step instructions below.

## Getting started

* Make sure you have a [GitHub account](https://github.com/signup/free).
* Submit a [ticket](https://github.com/gobridge/gobridge.github.io/issues) for your issue, assuming one does not already exist. Minor changes like fixing typos or other trivial things don't require opening a ticket.
* Fork the repository on GitHub and clone your repository on your local machine.

### Making changes

#### Refresh your local repo's source branch (not necessary if you just cloned it):

* ```git pull origin source```

#### Create a topic branch from the [source](https://github.com/gobridge/gobridge.github.io/tree/source) branch:

* ```git checkout source```(if you are not already in the source branch)
* ```git checkout -b 12-add-events-page``` (this example contains a hypothetical issue number and a short title)

#### Make your changes :boom:

This website is generated using Hugo. They have [excellent documentation](https://gohugo.io/overview/introduction/) to get you going.

####  <a name="runhugo"></a> Run Hugo and generate new static files that will reflect your changes:
* ```hugo ```

The generated content will be placed in the subtree public directory. Note that at this point, if you check the branch for differences, there should be none.

#### Visualize your changes on your local computer:
* ```hugo server```

Hugo will output a url that you can paste on your browser to see the live website.

## Submitting changes

* Make commits of logical units.
* Check for unnecessary whitespace with `git diff --check` before committing.
* Make sure your commit messages are in a [proper format](http://chris.beams.io/posts/git-commit, and include the issue number in the title).
* Push your branch.
* Make a pull request.

# Additional resources

* [General GitHub documentation](http://help.github.com/)
* [GitHub pull request documentation](http://help.github.com/send-pull-requests/)
* #gobridge channel on [Gophers Slack](https://gophers.slack.com/messages/gobridge) - [Invite Link](http://bit.ly/go-slack-signup)

---

## <a name="maintainers"></a> For Maintainers

### After fetching a pull request, start at the instructions above to [run Hugo](#runhugo) and generate the static files into the subtree public folder.

#### Pull down new files from the `master branch` into the `public`subtree folder (just in case they have diverged -- if they have, a merge will be needed). This will help avoid merge conflicts:
* ```git subtree pull --prefix=public git@github.com:gobridge/gobridge.github.io.git master```

#### Update the source content
* ```git push origin source```

#### Update the static files by pushing the public subtree to the master branch

* ```git subtree push --prefix=public git@github.com:gobridge/gobridge.github.io.git master```
