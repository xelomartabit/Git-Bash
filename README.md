# Git-Bash
# Git
## Set up
```bash
# install git, update y check
sudo apt-get install git
sudo apt-get update
git --version

# config git user email y check config
git config --global user.name "marcelo martabit"
git config --global user.email "mail@gmail.com"
git config --list

# token
settings > developer settings > personal access tokens (PAT) > (tokens classic) > generate new token (classic)
scopes check repo
```

## Local
```bash
# iniciar repo local
git init 

# vincular repo remota a nuestra repo local
git remote add origin <url>

# check status
git status

# add specific file / all 
git add <archivo>
git add .

# commit
git commit -m "mensaje"

# pushea los contenidos a github
git push origin main
git push -u origin main

# NOTA: renombra la rama actual a main
git branch -M main
```

## Remote
```bash
# Fork repo (recordar actualizar)
# clonar repo
git clone https://github.com/<User>/repo.git

# rama principal y actualiza
git checkout main
git pull origin main

# Sal de la rama principal e inicia una branch
git checkout -b <branch>

# check status
git status

# add specific file / all 
git add <archivo>
git add .

# actalizar el Fork con los datos nuevos del repositorio original
git remote add upstream https://github.com/<AdminRepo>/RepoOG.git
git fetch upstream
git checkout main
git merge upstream/main

# push
git push origin <branch>
```

## Bash
```bash
# Crear directorios
mkdir <nombre carpeta>

# Navegar entre carpetas
cd <Folder>, cd ..

# crear archivos
crear y abrir: nano <FileName.txt>
crear vacio: touch <FileName.txt>
crear con un print: echo "hola" > <FileName.txt>

# Mover
mv <File/Folder> <Destino>

# copiar
cp <File/Folder> <Destino>

# Listar archivos en carpeta actual
listar: ls
listar con permisos: ls -l <FileName.txt>
listar incluido ocultos: ls -a

# Ubicacion actual
pwd

# Eliminar archivos
rm

# Eliminar carpetas vacias
rd
rmdir

# borrar carpetas con contenido
rm -r <Folder>

# Buscar en texto
grep "word" <FileName.txt>

# print en pantalla
cat <FileName.txt>
multiple: cat <FileName.txt> <FileName.txt>
combinar en un archivo: cat <FileName.txt> <FileName.txt> > <FileName.txt> 

#buscar archivos
find
todos los archivos de un tipo: find *.txt

# Cambiar permisos
chmod
numeros:
solo yo rw: chmod 600 <FileName.txt>

# Ver permisos
chown

#comprimir
tar -czvf <directory.tar.gz> <FileName.txt>

#extraer
mkdir <directory>
tar -xzvf <directory.tar.gz> -C <directory>

# awk
awk -F "," '{print $1}' nombres.csv

```

# Python
```

```
