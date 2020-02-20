# ** GIT **

1. [Remove Submodule](#Number_1)
2. [Clone into exists folder](#Number_2)

### <a name="Number_1"></a> **Remove Submodule**

1. Delete the relevant line from the . gitmodules file.
2. Delete the relevant section from . git/config.
3. Run git rm --cached pathtosubmodule (no trailing slash).
4. Commit the superproject.
5. Delete the now untracked submodule files.

### <a name="Number_2"></a> **Clone into exists folder**

1. First get to the existing directory
```
$ cd my/folder/
```
2. Now start a new git repository
```
$ git init
```
3. Identify if the current elements on the directory are needed or not and add them to the .gitignore file. When ready…
```
$ vim .gitignore
```
4. When ready create the first commit on the server
```
$ git add .
$ git commit -m 'my first commit'
```
5. Now add the remote from where you want to clone
```
$ git remote add origin https|ssh:path/to/the/repository.git
```
6. Now just pull and merge with local git
```
$ git pull origin master
```
7. If you have some merge conflicts resolve them and commit your changes.

