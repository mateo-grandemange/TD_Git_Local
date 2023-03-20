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
Check in the web UI you see your branch
```
git log --graph --oneline
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

## Exercise 5: 

1. Pull the latest changes in the ’master’ branch, check the README.md
is up-to-date (contains all the paragraphs and the new line).
```
git pull origin master
```
2. Switch back to your own branch (not including the latest changes from
the master branch).
```
git checkout Matthieu
```
3. Merge the changes from ’master’ to your own branch.
```
git merge master
```
4. Commit this change.
```
git add README.md
git commit -am "New changes"
```

## Exercice 6 :

1. Delete your branch on local repository.
```
git branch -d Matthieu
```

2. Delete your branch on distant repository.
```
git push GIT-BRANCHES --delete Matthieu
```

## Exercice 7 :

1. Pull the latest changes in the ’master’ branch.
```
git checkout master
git pull origin master
```
2. Create a new local branch named after you and switch to it.
```
git checkout -b Matthieu
```
3. Then with a separate commit for each change 
(a) Clear the whole file, removing all text.
```
echo "" > README.md
git add README.md
git commit -m "Clear file"
git push origin Matthieu
```
(b) Add a title line "Git interactive rebase".
```
echo "Git interactive rebase" >> README.md
git add README.md
git commit -m "Add title"
git push origin Matthieu

```
(c) Copy the first paragraph from https ://git-scm.com/book/en/v2/Git-
Tools-Rewriting-History.
```
curl https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History | grep -oP "(?<=div class="\paragraph"\>).*(?=with others)" >> README.md
git add README.md
git commit -m "Copy the first paragraph"
git push origin Matthieu
```
(d) Add the second paragraph from the same page.
```
curl https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History | grep -oP "(?<=Changing your most).*(?=modifying files.)" >> README.md
git add README.md
git commit -m "Add the second paragraph"
git push origin Matthieu
```
(e) Add the first and second paragraphs from the "Changing Multiple
Commit Messages" section in the same page.
```
curl https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History | grep -oP "(?<=Changing your most).*(?=new last commit.)" >> README.md
git add README.md
git commit -m "Add the first and second paragraphs from the 'Changing Multiple Commit Messages' section in the same page."
git push origin Matthieu
```
(f) Remove the second paragraph from your file.
```
sed -i '16d' README.md
git add README.md
git commit -m "Remove the second paragraph "
git push origin Matthieu
```
(g) Add the missing title "Changing Multiple Commit Messages" 
```
sed -i '4i Changing Multiple Commit Messages' README.md
git add README.md
git commit -m "Add missing title"
git push origin Matthieu
```
(h) Add a final line with your name or alias.
```
echo "Matthieu JULIEN" >> README.md
git add README.md
git commit -m "Add name"
git push origin Matthieu
```
4. Use interactive rebase to have a single commit with message "Explain git
interactive rebase.".
```
git rebase -i HEAD~3
```
5. Push your branch on the remote repository.
```
git push origin Matthieu
```

## Exercice 8 :

Done on Github
