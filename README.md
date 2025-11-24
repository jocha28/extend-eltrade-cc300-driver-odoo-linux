# Eltrade CC300 Driver – Linux / Ubuntu

Un driver  pour communiquer avec l’imprimante **Eltrade CC300** sous Linux.  
Ce projet permet de compiler et exécuter un serveur local pour échanger avec l’appareil.

---

## Prérequis

Installer Go :

```bash
sudo apt update
sudo apt install golang-go
```

Vérifier :

```bash
go version
```

---

## Installation

Placer-vous dans le dossier :

```bash
cd eltrade-cc300-driver-master
```

Installer les dépendances :

```bash
go mod tidy
```

---

## Build

Compiler le driver :

```bash
go build -o eltrade-driver
```

---

## Exécution

Lancer le programme :

```bash
./eltrade-driver
```

URL par défaut :

```
http://localhost:8080
```

---

## Mise à jour après modification du code

Rebuild :

```bash
go build -o eltrade-driver
```

Relancer :

```bash
./eltrade-driver
```

---

## Script d’automatisation (optionnel)

Créer `rebuild.sh` :

```bash
#!/bin/bash
go build -o eltrade-driver && ./eltrade-driver
```

Rendre le script exécutable :

```bash
chmod +x rebuild.sh
```

Exécuter :

```bash
./rebuild.sh
```

---

## Structure du projet

```
.
├── bin/
├── cmd/
├── eltrade/
├── lib/
├── server/
├── main.go
├── Makefile
├── go.mod
├── go.sum
└── bill.spec.json
```

---

## Licence

Open-source – non affilié à Eltrade.
