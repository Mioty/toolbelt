# Mioty ToolBelt

It would be really cool to automate some of this like *Heroku* does it:

    heroku <some-command>

Possibly through some `npm install -g` magic. Look at [firebase-tools](https://github.com/firebase/firebase-tools) for guidance.

Until then, this doc will do.

## Requirements

Your gonna need some basic necessities like 

* [node/npm](http://nodejs.org/) recommended version `v0.10.33`
* [git](http://git-scm.com/) recommended version `v2.1.2`
* [Hipchat](https://www.hipchat.com/downloads)

Here is a good link to get you started with setting up your `git config -l`:
[Github and Git](http://burnedpixel.com/blog/beginners-setup-guide-for-ruby-node-git-github-on-your-mac/)               
\* *Disregard the ruby stuff. Also for the record, I dont recommend using `homebrew` to install node/npm. Things can get messy.*

Using `sudo` isn't recommended so:
```sh
sudo chown -R `whoami` /usr/local
```

While you're at it:
```sh
git config --global push.default simple
```

## Git Aliases

1. Copy/Paste the git aliases from [mioty.aliases](https://github.com/Mioty/toolbelt/blob/master/mioty.aliases) into your ~./gitconfig
2. See [ALIASES](https://github.com/Mioty/toolbelt/blob/master/ALIASES.md) for more info

- `git bl`
- `git blr`
- `git co`
- `git fe`
- `git fi`
- `git mi`
- `git up`
- `git cm`
- `git sync`
- `git bdone`

## Bash Profile 

Make your prompt look like:

```bash
me@my-pc ~/some/repo (branch-name) $
```

Add [mioty.bash_profile](https://github.com/Mioty/toolbelt/blob/master/mioty.bash_profile) to your ~./bash_profile

## Commiting 

Commits must follow [CONVENTIONS](https://github.com/Mioty/toolbelt/blob/master/CONVENTIONS.md)

- All repos should have allowed scopes in SCOPES.md
- By default, all repos will block any non-conforming commits. In order to bypass this check, use 'Work-In-Progress' syntax:

    ```sh
    WIP: <subject>
    ```
    
- You can clean up commits messages with:

    ```sh
    git rebase master -i
    ```
    
    then using `squash` (merge commit msg) or `reword` followed with:
    
    ```sh
    git push -f
    ```

## Pull Request

- If your branch falls behind *master* then use (see [note](https://github.com/Mioty/toolbelt/blob/master/ALIASES.md#notes) about conflicts):

    ```sh
    git sync
    ```
    
    if no conflicts:
    
    ```sh
    git push -f
    ```

## Hipchat

Each repo has a corresponding Hipchat room for git notifications, build updates, deployment status, etc...

*TODO* add hipchat repo commands









