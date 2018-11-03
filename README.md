# Atcoinwebsite

This is a work in progress. Website content is markdown served with Jekyll. Jekyll is a blog-aware, static site generator in Ruby.

## Get started

1. Install Ruby
2. Install Bundler: `gem install bundler`
3. Clone this repo
4. Go to project folder: `bundle install`
5. `jekyll serve`
6. Go to: http://127.0.0.1:4000/

## How to contribute.

We are looking for help with articles, design, transation, etc. Join us in #design [on Slack.](https://join.slack.com/t/anoncoin/shared_invite/enQtMjcxMzUxMjk5ODYwLTU0OTJhNmIxNzYyY2JiMzUxOGZhMjYzNmQ3YmViNWM1OWIxZGNlMGY0Zjg1NzdhMDAyZmRiYTFhNTM1OWZiYTU)

This is the basic process on how to contribute to the Atcoinwebsite.

## Creating a Fork

Just go to the top of the page and click the "Fork" button. It's just that simple. Once you've done that, you can use your favorite git client to clone your repo or just head straight to the command line:

```shell
# Clone your fork to your local machine
git clone git@github.com:USERNAME/FORKED-PROJECT.git
```

## Keeping Your Fork Up to Date

While this isn't an absolutely necessary step, if you plan on doing anything more than just a tiny quick fix, you'll want to make sure you keep your fork up to date by tracking the original "upstream" repo that you forked. To do this, you'll need to add a remote:

```shell
# Add 'upstream' repo to list of remotes
git remote add upstream https://github.com/UPSTREAM-USER/ORIGINAL-PROJECT.git

# Verify the new remote named 'upstream'
git remote -v
```

Whenever you want to update your fork with the latest upstream changes, you'll need to first fetch the upstream repo's branches and latest commits to bring them into your repository:

```shell
# Fetch from upstream remote
git fetch upstream

# View all branches, including those from upstream
git branch -va
```

Now, checkout your own master branch and merge the upstream repo's master branch:

```shell
# Checkout your master branch and merge upstream
git checkout master
git merge upstream/master
```

If there are no unique commits on the local master branch, git will simply perform a fast-forward. However, if you have been making changes on master (in the vast majority of cases you probably shouldn't be - [see the next section](#doing-your-work), you may have to deal with conflicts. When doing so, be careful to respect the changes made upstream.

Now, your local master branch is up-to-date with everything modified upstream.

## Doing Your Work

### Create a Branch
Whenever you begin work on a new feature or bugfix, it's important that you create a new branch. Not only is it proper git workflow, but it also keeps your changes organized and separated from the master branch so that you can easily submit and manage multiple pull requests for every task you complete.

To create a new branch and start working on it:

```shell
# Checkout the master branch - you want your new branch to come from master
git checkout master

# Create a new branch named newfeature (give your branch its own simple informative name)
git branch newfeature

# Switch to your new branch
git checkout newfeature
```

Now, go to town hacking away and making whatever changes you want to.

## Submitting a Pull Request

### Cleaning Up Your Work

Prior to submitting your pull request, you might want to do a few things to clean up your branch and make it as simple as possible for the original repo's maintainer to test, accept, and merge your work.

If any commits have been made to the upstream master branch, you should rebase your development branch so that merging it will be a simple fast-forward that won't require any conflict resolution work.

```shell
# Fetch upstream master and merge with your repo's master branch
git fetch upstream
git checkout master
git merge upstream/master

# If there were any new commits, rebase your development branch
git checkout newfeature
git rebase master
```

### Submitting

Once you've committed and pushed all of your changes to GitHub, go to the page for your fork on GitHub, select your development branch, and click the pull request button. If you need to make any adjustments to your pull request, just push the updates to GitHub. Your pull request will automatically track the changes on your development branch and update.


## Questions?

Join us in #design [on Slack and ask.](https://join.slack.com/t/anoncoin/shared_invite/enQtMjcxMzUxMjk5ODYwLTU0OTJhNmIxNzYyY2JiMzUxOGZhMjYzNmQ3YmViNWM1OWIxZGNlMGY0Zjg1NzdhMDAyZmRiYTFhNTM1OWZiYTU)
