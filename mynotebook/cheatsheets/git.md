# Git cheatsheet

I finished my modifications, I want to commit and push to repository
```{code-cell}
git status // Permet de voir tous les fichiers qui ont été modifiés.
git add . // Permet d'ajouter au commit toutes les modifications qui ont été faites. Un git status permet de voir que tous les fichiers sont sous "Changes to be committed:"
git commit -m "[ADD] my comment"
git push origin branchname
```

In the Github web interface I created an issue, and then a merge request with a new branch. Now I want to get this branch locally and and start to code in it.
```{code-cell}
git fetch origin
git checkout 5-add-kotlin-basics
```
