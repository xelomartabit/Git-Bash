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
tar -czvf <archive.tar.gz> <FileName.txt>
    -c is creating and archive.
    -z is using gzip compression.
    -v is providing details of the files that have been archived.
    -f is creating an archive with the name 'logs_archive.tar.gz' as supplied in the command above.

remove files: tar -czvf <archive.tar.gz> * --remove-files
view the contents of an archive: tar -tvf <archive.tar.gz>

search in compressed files: zgrep -Hna 'string-to-search' <archive.tar.gz>
    -H lists the file name that contains the match.
    -n displays the line number that contains the matched string.
    -a treats all files as text files. 

#extraer
mkdir <directory>
tar -xzvf <archive.tar.gz> -C <directory>
    -x is extracting and archive.
    -z specifies that the archive is gzip.
    -v is providing details of the files that have been archived.
    -f is extracting from the archive named 'logs_archive.tar.gz'.

# awk
awk '{print $0}' information.txt
line-number count NR: awk '{print NR,$0}' information.txt
more than one column: awk '{print $1, $4}' information.txt
specific lines of a column: awk '{print $1}' information.txt | head -1
awk -F "," '{print $1}' nombres.csv

```

# Python open()
```python
To save a variable to a `.txt` file on Linux using Python, you can use the built-in `open()` function along with the `write()` method. Here's a basic example:

### Example:
# Variable you want to save
my_variable = "Hello, this is the content I want to save."

# Open a text file in write mode and save the variable
with open("output.txt", "w") as file:
    file.write(my_variable)

This will create a file named `output.txt` in the same directory where the script is run, and write the contents of `my_variable` into it.

If your variable is not a string (e.g., a list or dictionary), you should convert it first using `str()` or `json`:

```
