# After Git clone from GitHub, I do not see my branch
By default, git clone creates only one branch: the currently checked out one, generally master. However, it does create remote tracking branches for all other branches in the remote. Think of these as local copies of the remote's branches, which can be updated by fetching. They're not real local branches, as they're intended only as pointers to where the remote's branches are, not for you to work on.

If you run git branch -a you'll see all branches, local and remote. If you want to see just the remote ones, use git branch -r. If you prefer a visual history display, try gitk --all (or gitk --remotes).
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch -a
* main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
  remotes/origin/v1-user-management-app
  remotes/origin/v2-country-app

```

To create a local branch to work on, use

git branch <branch-name> origin/<branch-name>
That'll create a new local branch using the remote's branch as the starting point.
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch v1-user-management-app origin/v1-user-management-app

```
Now you can see branch on local
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch
* main
  v1-user-management-app

```

sudo apt-get install python-dev python3-dev
sudo apt-get install libmysqlclient-dev
pip install pymysql
pip install mysqlclient

# config vim editor
```
atul@atul-Lenovo-G570:~$ git config --global core.editor vim
```
# Create a new branch
1. First of all check branch already created or not. * show before main it means you are in the main branch.
   ```
   (venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch
   * main
  v1-user-management-app
  v2-country-app

```
2. If branch is not created then create new branch
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch v3-state-app

```
3. Again check breach create or not
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch
* main
  v1-user-management-app
  v2-country-app
  v3-state-app

```
4. Now go in newly created branch
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git checkout v3-state-app
Switched to branch 'v3-state-app'

```
5. Again check brach. * show before v3-state-app brach it means you are in the v3-state-branch
```
(venv) atul@atul-Lenovo-G570:~/mydjangofirst/derp$ git branch
  main
  v1-user-management-app
  v2-country-app
* v3-state-app

```
