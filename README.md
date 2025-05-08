# Git-Bash
hola

## install git, update and check version
```bash
# install git, update y check
sudo apt-get install git
sudo apt-get update
git --version

# config git user email y check config
git config --global user.name "marcelo martabit"
git config --global user.email "mail@gmail.com"
git config --list
```

## Remote
```bash
# clonar repo
git clone https://github.com/<User>/Fork.git

# Sal de la rama principal e inicia una branch
git checkout main
git pull origin main
git checkout -b <branch>

# actalizar el Fork con los datos nuevos del repositorio original
git remote add upstream <https://github.com/><AdminRepo>/RepoOG.git
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```
