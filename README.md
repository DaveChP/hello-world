# hello-world
An addition made in the local repository AFTER an earlier addition made to origin

My oh my, grapling security keys can be frustrating. Thank goodness for github's documents pages.

I used the default correction for a failed pull due to changes on remote version. Then pulled. merge failed by conflicts. Opened file in vim, deleted pink bits (except the title) and added some text here

Another local edit to add double returns to text file for markdown paragraphs

## Summary of pull/push so far
I had made an edit to README using the github online editor. I also modified the file locally (so the versions differ by new edits on both). I tried to push the local file to remote:

```git push origin```
```> ! [rejected] ...```

Terminal message explained the remote copy contains work that is not in the local copy. Suggesting that remote changes are first integrated locally

```
git pull origin main
```

The following hints were included in the terminal message:

```
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint: 
hint:   git config pull.rebase false  # merge (the default strategy)
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint: 
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
```

And then:

```
fatal: Need to specify how to reconcile divergent branches.
```

I used the first suggestion in the hints:

```
git config pull.rebase false
```

and repeated the pull request:

```
git pull origin main
```

I got a terminal message warning that automatic merge failed due to conflics and instructed me to reconcile differences before merge.

Having edited the text file, following messages about diverged files, I addded and committed the local README to the local repository before pushing it to remote:

```
git push origin main
```

Latly, I added these summary notes locally and will not push them with the same command. (nothing should have changed online since).
