
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
git tab -l
```

Tags que contienen este commit:
```
git tag --contains 813d21e118eebf184fc6eb7667872b1eaeb9c86a
```
