# How to contribute

Note: Maintainers of this repository have [additional instructions for maintainers](#maintainers) on how to deploy the website.

----------
The GoBridge website contains information for people interested in learning about what we do and who we are, our scheduled events, how to contact us, etc.

As with all of our resources, this is a community driven work by volunteers and for volunteers who benefit from GoBridge. This means YOU! If you are interested in improving the UX and/or design of the website, we encourage you to do so and hope to make your process of contributing as easy as possible with the detailed step-by-step instructions below.

## Getting started

* Make sure you have a [GitHub account](https://github.com/signup/free).
* Submit a [ticket](https://github.com/gobridge/gobridge.github.io/issues) for your issue, assuming one does not already exist. Minor changes like fixing typos or other trivial things don't require opening a ticket.
* Fork the repository on GitHub and clone your repository on your local machine.

### Making changes

#### Refresh your local repo's master branch (not necessary if you just cloned it):

* ```git pull origin master```

#### Create a topic branch:

* ```git checkout -b 12-add-events-page``` (this example contains a hypothetical issue number and a short title)

#### Make your changes :boom:

This website is generated using Hugo. They have [excellent documentation](https://gohugo.io/overview/introduction/) to get you going.

####  <a name="runhugo"></a> Run Hugo and generate new static files that will reflect your changes:
* ```hugo ```

The generated content will be placed in the `public/` directory. Note that at this point, if you check the branch for differences, there should be none.

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
* #gobridge channel on [Gophers Slack](https://gophers.slack.com/messages/gobridge) - [Invite Link](https://gophersinvite.herokuapp.com/)

---

# Maintainers

The website is hosted on [Netlify](https://app.netlify.com/sites/gobridge-dot-org).

Merges into the `master` branch are automatically rendered and deployed to golangbridge.org by Netlify.

If you wish to preview the rendered version of a PR, fetch the PR and follow the instructions above to [run Hugo](#runhugo).

The `public/` directory is ignored by git. There is no need to check it in as Netlify will generate it automatically.

PR's are automatically rendered by Netlify and are available publicly via the following URL pattern: `http://deploy-preview-<PR#>.gobridge-dot-org.netlify.com/` (eg. For PR#3, the url would be `http://deploy-preview-3.gobridge-dot-org.netlify.com/`).

Notifications are pushed to #gobridge-ops on Slack and include preview links.
