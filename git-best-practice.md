# GIT Best Practices

    The objective of the document is to harmonize team members' use of the git conventions.

## Branch Naming convention

A branch name convention is used to avoid confusion and make it simple for team members to recognise the work that is linked.

<span style="color:red">Don't</span>

```
fix-bug

create-employee

task1012
```

<span style="color:green">Do:</span>

Task/Bug/Refactor ID - 1012

```
fix-1012

task-1012

refactor-1012

```

IF no task ID

```
fix-login

task-create-user

refactor-user-api

```

## Commit Message convention

<type>:<scope> - <short summary>

Example

```
feat:user-api - list user role api with pagination

fix:auth-api - login based on role issue fix

```

### Type

1. **feat** - Anything new will be a feature related to UI, Style, Feature,

2. **fix** - Business Logic and Bugs (reported or not reported) Prod or non-prod.

3. **refactor** - Any code refactoring or Improvements

4. **test** - Adding missing tests or correcting existing tests

5. **style** - Changes that do not affect the meaning of the code (white space, formatting, missing semi-colons, etc)

6. **build** - Build related changes or issue

### Scope

The scope should be the module's name to which the changes are unavoidable,

Example

```
dashboard, login, signup, home, user, customer, and product.
```

### Short Summary

Summary in the present. without capitalization. There is no period at the end.

## VSCode GIT Source Control

### Pull from Repo

1. Use the source control view to pull changes from a remote repository.
2. Click on the "View more" option in the source control panel and select "Pull" from the dropdown menu.
3. This action will fetch and incorporate the changes from the remote repository into your local environment.
4. Before pulling changes from a remote repository, ensure that you are on the correct branch. You can check the current branch in the left-end corner of VS Code.
5. Always synchronize changes by clicking on the icon at the left-end corner after the branch name before pulling from the current branch.

Check this [video](./assets/videos/Git%20pull%20-%20Demo%20using%20VS%20Code.mp4) for demo.

## Push from Repo

1. Use the source control view to push your local commits to a remote repository.
2. First, you need to stage the files you want to push in the source control.
3. Then, add a commit message in the message text box in the source control.
4. Click on the "View more" option in the source control panel and select "Push" from the dropdown menu.
5. This action will push the local commits to the remote repository.
6. Before pushing changes to a remote repository, verify the current branch you are on in the left-end corner of VS Code.
7. Always synchronize changes by clicking on the icon at the left-end corner, next to the branch name, before pushing to the current branch.

Check this [video](./assets/videos/Git%20Push%20-%20Demo%20using%20VS%20Code.mp4) for demo.
