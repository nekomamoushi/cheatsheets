# Configuration

```
$ git config --global user.name "jerome"

$ git config --global user.email "jp@hotmail.com"

$ git config --global core.editor gvim

$ git config --global merge.tool filemerge

$ git config --list
```

# Status des fichiers

```
$ git status
```

# Lister les branches

```
$ git branch
```

# Creer une branche

```
$ git branch nom_de_ma_branch
```

# Changer de branch

```
$ git checkout nom_de_ma_branch
```

# Premier commit

```
$ git add .
$ git commit - m "initial commit"
```

# Commit suivant

```
$ git add chemin_vers_mon_fichier
$ git commit -m "message du commit"
```

# Diff

Affiche la difference entre le contenu du dernier commit et celui du repertoire de travail.
Cela correspond a ce qui serait commite par git commit -a.

```
$ git diff HEAD

$ git diff A B
```

# Log

```
$ git log

$ git log -n X

$ git log --since=date --until=date

$ git log --oneline --graph --decorate

$ git log --oneline --graph --decorate nom_du_fichier
```

# Annuler commits (soft)

Seul le commit est retiré de Git ; vos fichiers, eux, restent modifiés. Vous pouvez alors a nouveau changer vos fichiers si besoin est et refaire un commit.
Annuler le dernier commit

```
$ git reset HEAD^
```

Pour indiquer a quel commit on souhaite revenir, il existe plusieurs notations

HEAD : dernier commit ;
HEAD^ : avant-dernier commit ;
HEAD^^ : avant-avant-dernier commit ;
HEAD~2 : avant-avant-dernier commit (notation équivalente) ;
d6d98923868578a7f38dea79833b56d0326fcba1 : indique un numéro de commit précis ;

# Annuler commits (hard)

Si vous voulez annuler votre dernier commit et les changements effectués dans les fichiers, il faut faire un reset hard.
Cela annulera sans confirmation tout votre travail !

Annuler les commits et perdre tous les changements

```
$ git reset --hard HEAD^
```

Annuler les modifications d'un fichier avant un commit

Si vous avez modifié plusieurs fichiers mais que vous n'avez pas encore envoyé le commit et que vous voulez restaurer un fichier tel qu'il était au dernier commit :

```
$ git checkout nom_du_fichier
```

Annuler/Supprimer un fichier avant un commit

Supposer que vous venez d'ajouter un fichier a Git avec "git add" et que vous vous appréte a le commiter.
Cependant, vous vous rendez compte que ce fichier est une mauvaise idée et vous voulez annuler votre "git add' .
Il est possible de retirer un fichier qui avait été ajouté pour etre commité en procédant comme suit :

```
$ git reset HEAD -- nom_du_fichier_a_supprimer
```
