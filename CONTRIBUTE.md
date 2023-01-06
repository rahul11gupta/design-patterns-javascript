> Welcome! We love receiving contributions from our community, so thanks for stopping by! There are many ways to contribute, including submitting bug reports, improving documentation, or contributing code that can be incorporated into the project.

## Getting Started

> You will need to fork the main repository to work on your changes. Simply navigate to our GitHub page and click the "Fork" button at the top. Once you've forked the repository, you can clone your new repository and start making edits.

> In git it is best to isolate each topic or feature into a “topic branch”. While individual commits allow you control over how small individual changes are made to the code, branches are a great way to group a set of commits all related to one feature together, or to isolate different efforts when you might be working on multiple topics at the same time.

> While it takes some experience to get the right feel about how to break up commits, a topic branch should be limited in scope to a single issue

```
# Checkout the master branch - you want your new branch to come from master
git checkout master

# Create a new branch named newfeature (give your branch its own simple informative name)
git branch newfeature

# Switch to your new branch
git checkout newfeature
```

## Pull Request Process

Do you have any labelling conventions?

Add notes for pushing your branch:
Please include a summary of the change and which issue is fixed. Please also include relevant motivation and context. List any dependencies that are required for this change.

> When you are ready to generate a pull request, either for preliminary review, or for consideration of merging into the project you must first push your local topic branch back up to GitHub:

```
git push origin newfeature
```

Include a note about submitting the PR:

> Once you've committed and pushed all of your changes to GitHub, go to the page for your fork on GitHub, select your development branch, and click the pull request button. If you need to make any adjustments to your pull request, just push the updates to your branch. Your pull request will automatically track the changes on your development branch and update.

At the end of the note make sure to add the below template in your pull request:

### Type of change

Please delete options that are not relevant.

- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New design pattern addition
- [ ] Addition of a new example in an exisiting pattern
- [ ] Documentation update



### Checklist:

- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] Any dependent changes have been merged and published in downstream modules

## Addressing Feedback

Once a PR has been submitted, your changes will be reviewed and constructive feedback may be provided. Feedback isn't meant as an attack, but to help make sure the highest-quality code makes it into our project. Changes will be approved once required feedback has been addressed.

If a maintainer asks you to "rebase" your PR, they're saying that a lot of code has changed, and that you need to update your fork so it's easier to merge.

To update your forked repository, follow these steps:

```
# Fetch upstream master and merge with your repo's master branch
git fetch upstream
git checkout master
git merge upstream/master

# If there were any new commits, rebase your development branch
git checkout newfeature
git rebase master
```

If too much code has changed for git to automatically apply your branches changes to the new master, you will need to manually resolve the merge conflicts yourself.

Once your new branch has no conflicts and works correctly, you can override your old branch using this command:

```
git push -f
```

Note that this will overwrite the old branch on the server, so make sure you are happy with your changes first!

