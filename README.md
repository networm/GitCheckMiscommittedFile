# Git Check Miscommitted File

## Introduction

We always have some files which don't want to be changed and commited erroneously.

We could check it either before commit or push to repository. But I think the former one need to setup a `pre-commit` hook on everyone's repository. And the latter one only needs to deploy to server.

Check and reject any push which contains wrong file filtered by rules in commits.

If you want to commit protected files, you should add protected file's name in first line of commit message. Because script only checks title to ensure intention.

## Usage

Just put `update` in `repository/hooks` or server or `repository/custom_hooks` on GitLab.

## Custom

You could easily add custom rules in `rules` array of script. You could use either wildcard or path rules.

```
$rules =
[
  "ProjectSettings/*",
  "Assets/Resources/Yourfile.example",
]
```
