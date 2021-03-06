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

I got a terminal message warning that automatic merge failed due to conflicts and instructed me to reconcile differences before merge.

Having edited the text file, following messages about diverged files, I added and committed the local README to the local repository before pushing it to remote:

```
git push origin main
```

Lastly, I added these summary notes locally and will now push them with the same command. (nothing should have changed online since).

## online editing
The push worked properly.
After correcting a few typos online, I added these notes and will shortly pull this version to my local repo to work on (this time, nothing has changed locally so hopefully, this version will merge automatically.

## local
I pulled this file back to local using:

```
git pull origin main
```

running `git status` showed local up to date, implying remote was successfully merged to the local repo automatically. Opening this file locally in vim, showed the remote changes were indeed present. 

After adding these comments locally, I'll add, commit, and push the file back to the remote repository.


## Local Pull and Branch
04 May 2022, in the local repository I ran:

```
git pull origin main
```
message said, `already up to date` indicating no modifications to remote version since my last local changes.

To work on this file, I first created and checked-out a new branch, using the combined command:

```
git checkout -b local
```
this created, and moved to (by `checkout`), a new branch `-b`, called `local`

I've now opened the Readme file and am editing it before attempting to push it (without merging) back to the remote repository. 

I will attempt:
```
git push origin local
```
