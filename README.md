# <p align="center">vaccine</p>
> *Projet d'introduction à la compréhension d'une faille web très connue, la fameuse injection SQL (SQLi). Vous devrez créer un outil pour automatiser vos actions.*
>
> *Nous savons tous combien un développement sécurisé est important. Dans ce contexte, vous essaierez de trouver des erreurs de filtrage dans les entrées de données. L'injection SQL consiste à injecter des commandes SQL pour modifier le comportement d'un programme et exécuter des commandes sur la base de données.*
>
> *Dans ce projet, vous allez créer un outil capable de détecter les injections SQL à partir d'une URL.*

## Checklist
- MySQL
    * [x] Stacked queries
    * [x] Union-based
    * [x] Error-based
    * [x] Blind-based
- Microsoft SQL Server
    * [x] ~~Stacked queries~~
    * [x] Union-based
    * [x] Error-based
    * [x] Blind-based
- PostgreSQL
    * [x] ~~Stacked queries~~
    * [x] Union-based
    * [x] Error-based
    * [x] Blind-based
- SQLite
    * [x] ~~Stacked queries~~
    * [x] Union-based
    * [x] ~~Error-based~~
    * [x] Blind-based

## Install
```bash
sudo apt update -y
sudo apt install -y make
sudo apt install -y docker.io
sudo apt install -y libcurl4-openssl-dev
sudo apt install -y libjsoncpp-dev
```
```bash
link=Skalyaeve/vaccine
name=vaccine

git clone https://github.com/$link.git $name
cd $name && make
# run les conteneurs test:
sudo make docker # ça va être plutôt long
```

## Usage
```bash
./Vaccine -t mysql http://localhost:4242
less archive.json
```
```bash
rm archive.json
./Vaccine -t postgresql http://localhost:4343
less archive.json
```
```bash
rm archive.json
./Vaccine -t sqlite http://localhost:4444
less archive.json
```
```bash
rm archive.json
./Vaccine -t microsoftsql http://localhost:4545
less archive.json
```
```bash
sudo make docker-stop
sudo make docker-fclean
make fclean
```

