# Clase 02 - Git Desarrollo Colaborativo

## .gitignore
Me permite indicar los archivos o carpetas que quiero que no formen parte del repositorio. Por ejemplo archivos de log durante desarrollo, archivos temporales, etc.

**Se crea el archivo .gitignore dentro de la raíz del proyecto.**

## .gitkeep
Ayuda a git a versionar carpetas que quiero que sean parte del repositorio pero están vacías.

**Se crea el archivo .gitkeep dentro de la carpeta que quiero que git versione**

## RAMAS (BRANCHES)
Las ramas me permiten trabajar en diferentes partes del proyecto de manera auxiliar sin afectar las funcionalidades (código fuente que ya funciona)

### Listar ramas locales

```sh
git branch
```

### Listar ramas remotas

```sh
git branch -r
```

### Listar ramas locales y remotas

```sh
git branch -a
```

## Otra manera de hacer un commit 
Para agregar más información sobre lo que hizo dentro de ese commit (A partir de la tercera linea)

1. Muevo los archivos al staging area

```sh
git add <nombre/archivo>
```

2. Hago un commit

```sh
git commit # Eso abre el nao/vim/vsc para que escribamos el mensaje
```

3. Una vez escrito el mensaje para confirmar

Ctrl + O + Enter (guardar) | Ctrl + x

## Creando una rama (Creando una bifurcacion)

```sh
# primera alternativa
git branch feature/ramas # Crea una rama
git switch feature/ramas # Me muevo que indico
# segunda alternativa
git switch -c feature/ramas # Crear una rama y moverse a esa rama
```

## Como saber la diferencia entre 2 ramas

```sh
git diff <nombre-rama>
# En main y quiero ver la diferencia entre main y feature/ramas
git diff feature/ramas
```

## Fusionar 2 ramas
**IMPORTANTE:** Siempre que quiera traerme los cambios de una rama a otra. Tengo que estar ubicado en la rama donde quiero traerme los cambios.
O sea, que si quiero traerme lo que esta en feature/ramas a la rama main. Tengo que estar ubicado en la rama main.

