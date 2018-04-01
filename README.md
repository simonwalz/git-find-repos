# git-find-repos

A script to list status of all repositories located in subdirectories.

## Usage: git-find-repos

```sh
git find-repos [ADDIONAL_GIT_STATUS_OPTS]
git-find-repos [ADDIONAL_GIT_STATUS_OPTS]
```

##### Options
<table>
  <thead>
  <tr>
    <th>Option</th>
    <th>Description</th>
  </tr>
  </thead>
  <tbody>
  <tr>
    <td>Addional git-status options</td>
    <td>(optional) See <a href="https://git-scm.com/docs/git-status">git-status Dokumentation</a></td>
  </tr>
  <tr>
    <td><code>-u[UNTRACKED_FILES_MODE]</code></td>
    <td>(optional) E.g. untracked files mode:<br><code>no</code> - Show no untracked files (default)<br><code>normal</code> - Shows untracked files and directories<br><code>all</code> - Also shows individual files in untracked directories.</td>
  </tr>
  </tbody>
</table>

##### Example


```sh
git find-repos -uall
```

List all untracked files in all repositories.

##### Hint

The command can be used with [git2](https://github.com/simonwalz/git2). Just run the following command to find all git2 based repositories:

```sh
git2 find-repos [ADDIONAL_GIT_STATUS_OPTS]
```


## Usage: git-extended-status (helper)

The script `git-find-repos` uses a helper script to display the status of a repository. This script can be used individually.

```sh
git extended-status [ADDIONAL_GIT_STATUS_OPTS]
git-extended-status [ADDIONAL_GIT_STATUS_OPTS]
```

Options: see [Usage: git-find-repos](#usage-git-find-repos)

Changed default untracked files mode to: Show no untracked files.



## Speed up git-find-repos

git-find-repos fetches from remote repositories. [See this article](http://interrobeng.com/2013/08/25/speed-up-git-5x-to-50x/) on how to speed up git ssh connections. I added the following files to my `.ssh/config` file:

```ssh_config
Host github.com
        User git
        ControlMaster auto
        ControlPath ~/.ssh/s/m-%r@%h:%p
        ControlPersist 120s

Host gitlab.*
        ControlMaster auto
        ControlPath ~/.ssh/s/m-%r@%h:%p
        ControlPersist 120s
```
