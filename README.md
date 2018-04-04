# Git Flow Work Flow using GitKraken

This document describes the Git Flow workflow using GitKraken v3.5.0.

An asterisk (*) indicates that a procedure is defined elsewhere in the
document.

``` pseudo
procedure: Git Flow work flow
  create and initialize Git repository *
  initialize Git Flow in repo *
  do
    do
      start a feature *
      do
        edit code
        commit code *
      while feature needs work
      finish the feature *
    while new version not ready for a release
    release version *
    if a critical bug is found
      create a hotfix *
    endif
  while a project is still supported
done
```

``` pseudo
procedure: create and initialize Git repository
  select File->Init Repo
      (or [Ctrl]+I)
  select 'GitHub.com'
  select GitHub account
  enter repository name
      (use same rules as for creating a directory: no spaces, etc)
  enter a short description of the project
  select access type (public or private)
  check 'Clone after init'
  select (browse) where to clone to
  confirm that full path is correct
  select .gitignore template (optional)
  select license (optional)
  select [Create Repository and Clone]
done
```

``` pseudo
procedure: initialize Git Flow in repo
  select File->Preferences
      (or hamburger->Preferences)
      (or [Ctrl]+,
  select Git Flow
  fill in the form
      (the default values are usually OK)
  select [Initialize Git Flow]
done
```

``` pseudo
procedure: start a feature
  open the Git Flow panel *
  select [Feature] in the 'Start' column
  enter a feature name after 'feature/'
      (use same rules as for creating a directory: no spaces, etc)
  select the 'Latest develop' radio button
  select [Start Feature]
done
```

``` pseudo
procedure: commit code
  if in a rush
    express commit *
  else
    long commit *
  end if
done
```

``` pseudo
procedure: finish the feature
  if in a rush
    right-click on 'feature/...'
    select 'Finish feature/...'
  else
    open the Git Flow panel *
    select [Feature] in the 'Finish' column
        (or select [Finish feature/...]
  endif
  uncheck 'Rebase on develop'
  check 'Delete branch'
  select [Finish Feature]
done
```

``` pseudo
procedure: release version
  open the Git Flow panel *
  select [Release] in the 'Start' column
  enter a release name after 'release/'
      (eg. 'release/1.0')
  select the 'Latest develop' radio button
  select [Start Release]
  prepare for final release
      (eg enter and commit release notes)
  finish the release *
done
```

``` pseudo
procedure: create a hotfix
  open the Git Flow panel *
  select Hotfix in the 'Start' column
  enter a hotfix name after 'hotfix/'
      (eg. 'hotfix/1.0.1)
  select [Start Hotfix]
  do
    edit code
    commit code *
  while bug still exists
  finish the hotfix
done
```

``` pseudo
procedure: open the Git Flow panel
  mouse over 'GIT FLOW' in the left panel
  click on the right arrow that appears
done
```

``` pseudo
procedure: express commit
  enter commit message into the '// WIP'
  press [Ctrl]+[Shift]+[Enter]
done
```

``` pseudo
procedure: long commit
  in 'Unstaged Files', select [Stage all changes]
  in 'Commit Message' enter a summary of the changes
  if a longer description is desired
    enter a description of the changes
  endif
  select [Commit changes to ...]
done
```

``` pseudo
procedure: finish the release
  if in a rush
    right-click on 'release/...'
    select 'Finish release/...'
  else
    open the Git Flow panel *
    select [Release] in the 'Finish' column
        (or select [Finish release/...])
  endif
  if a custom tag message is desired
    enter tag message
  else
    leave tag message blank
        (default tag message is release name eg. 1.0)
  endif
  check 'Delete branch'
  select [Finish Release]
done
```

``` pseudo
procedure: finish the hotfix
  if in a rush
    right-click on 'hotfix/...'
    select 'Finish hotfix/...'
  else
    open the Git Flow panel *
    select [Hotfix] in the 'Finish' column
        (or select [Finish hotfix/...])
  endif
  if a custom tag message is desired
    enter tag message
  else
    leave tag message blank
        (default tag message is hotfix name eg. 1.0.1)
  endif
  check 'Delete branch'
  select [Finish Hotfix]
done
```

Source: https://blog.axosoft.com/gitflow/
