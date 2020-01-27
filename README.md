
#  Algunos comandos útiles de GIT


##  TAGS (releases)


Vista de arbol de commits y tags en consola:

```
git log --graph --full-history --all --color \
        --pretty=format:"%x1b[31m%h%x09%x1b[32m%d%x1b[0m%x20%s"
```


Muestra las releases y su respectivo commit (Mejorable):

```
git tag -l |while read linea ; do echo "$(git rev-list -n 1 $linea), $linea"; done
```

Muestra las releases:

```
git tag -l
```

Tags que contienen este commit:
```
git tag --contains 813d21e118eebf184fc6eb7667872b1eaeb9c86a
```


Obtener una release concreta:

```
$ git checkout tags/v1.1.0
Note: checking out 'tags/v1.1.0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>
```

