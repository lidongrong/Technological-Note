## Some easy tips for getting started with Git

### Clone a repository from github

```
git clone https://github.com/lidongrong/Technological-Note
```

This will download the repository to local and you may find it in the dictionary you are currently in

### Set up user config

```
git config user.name yourname
git config user.email youremail@youremamil.com
```

### Make some changes and commit it to the main branch

You can make some changes to the repository, and then commit this change to the main branch, and then push this change to the repository at github

```
# Assume that I've adjusted the file GitNote
git add GitNote
git commit -m "The reason you would like to comment"
```

Then push this back to the repository online:

```
git push origin
```

Some more features will be recorded later