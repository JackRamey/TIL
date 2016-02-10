Global gitignore
================

There are commonly system files that pop up regularly that are repeatedly added to
a project's .gitignore file. You can create a global gitignore file on your system
that will be applied to all git projects on that system.

```
touch ~/.gitignore_global
git config --global core.excludesfile ~/.gitignore_global

```