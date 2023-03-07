# TD : Git branches

## Exercice 1 :

Using only command-line in your Linux shell, clone it to a local reposi-
tory.
```
git clone https://github.com/mateo-grandemange/TD_Git_Branches
```

## Exercice 2 :

1. Create a branch named after you.
```
git branch antoine_matthieu_mateo
```

2. Create a new text file named after you (with the content you want).
```
echo "Bonjour" > antoine_matthieu_mateo.txt

```
3. Commit this new file.
```
git add antoine_matthieu_mateo.txt
git commit -m "Done"
```
4. Push your branch to the remote repository
```
git push origin Matthieu
#Then enter access token
```

## Exercice 3 :

1. Merge your branch into the ’master’ branch.
```
git checkout master  #To switch to the master branch
git merge Matthieu
```
2. Push your changes in the ’master’ branch to the remote repository.
```
git push origin master
```

## Exercice 4 :

1. Switch back to your own branch (not including the latest changes from
the master branch).
```
git checkout Matthieu
```
2. Edit the lines 2 to 6 of the README.md file with a text you like (a
poem, a quote, some clever code...). It can be any readable text, it may
be incomplete, it must just take about 5 lines and be different from your
teammates. It must start on line 2 to trigger conflicts between team
members.
```
vim README.md    #To modify README.md
```
3. Commit this change.
```
git add README.md
git commit -m "Update de Matthieu on README.md"
```
4. Pull latest status from the remote repository ’master’ branch into your
local ’master’ branch. 
```
git checkout master
git pull origin master
```
5. Merge your branch into the local ’master’ branch. 
```
git merge Matthieu
```
6. If there are conflicts, we want the paragraph to appear in alphabetical
order in the final README.md file.
```
sort README.md > README_sorted.md
```
7. Push your changes in the ’master’ branch to the remote repository.
```
git push origin master
```
