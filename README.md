# git-find-repos

A script to list status of all repositories located in subdirectories.

## Usage: git-find-repos

```sh
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


## Usage: git-extended-status (helper)

The script `git-find-repos` uses a helper script to display the status of a repository. This script can be used individually.

```sh
git-extended-status REPO_PATH [ADDIONAL_GIT_STATUS_OPTS]
```

Changed default untracked files mode to: Show no untracked files.

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
    <td><code>REPO_PATH</code></td>
    <td>Local path to the git repository.<br>Default: current directory</td>
  </tr>
  <tr>
    <td>Addional git-status options</td>
    <td>(optional) See <a href="https://git-scm.com/docs/git-status">git-status Dokumentation</a></td>
  </tr>
  <tr>
    <td><code>-u[UNTRACKED_FILES_MODE]</code></td>
    <td>(optional) E.g. untracked files mode:<br><code>no</code> - Show no untracked files (default)<br><code>normal</code> - Shows untracked files and directories<br><code>all</code> - Also shows individual files in untracked directories.</td>
  </tr>
  </tr>
  </tbody>
</table>
