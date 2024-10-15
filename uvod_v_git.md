# Basic Git Instructions

## Naloga 1: Ustvarite svoj prvi repozitorij
### Navodila:
1. Odprite terminal.
2. Pomaknite se v mapo, kjer želite ustvariti git repozitorij.
3. Inicializirajte nov Git repozitorij.

### Rešitev:
```sh
cd /pot/do/vaše/mape
git init
```

### Smiselne bližnice za uporabo terminala:
1. Uporabite `cd ~` za hitro vrnitev v domačo mapo.
2. Uporabite `cd -` za preklop nazaj na prejšnjo mapo.
3. Uporabite `cd ..` za premik eno raven višje v drevesni strukturi.
4. Uporabite `cd /pot/do/imenika` za neposreden dostop do določene mape.
5. Uporabite `cd` brez argumentov za vrnitev v domačo mapo.
6. Uporabite tipko `Tab` za samodejno dopolnjevanje imen datotek in map.
7. Uporabite `cd /` za premik v korensko mapo.
8. Uporabite `cd ../..` za premik dve ravni višje v drevesni strukturi.
8. Uporabite `Ctrl + L` za čiščenje zaslona terminala.
9. Uporabite `Ctrl +` za povečavo besedila v terminalu.“““



## Naloga 2: Potisnite svoj prvi commit
### Navodila:
1. Ustvarite novo datoteko v svojem repozitoriju.
2. Dodajte datoteko v območje za pripravo (staging area).
3. Commitajte datoteko.
4. Potisnite commit v oddaljeni repozitorij.

### Osnovne komande:
```sh
git status # preveri katere datoteke so nove
git add . # dodaj vse datoteke
git commit -m "komentar" # dodaj komentar in komitnej
```

### Rešitev:
```sh
echo "# Moj prvi repozitorij" > README.md
git add README.md
git commit -m "Prvi commit"
git branch -M main #-M automatically renames the master branch to main.
git remote add origin https://github.com/vašeuporabniškoime/vaš-repo.git
git push -u origin master
```

### Dodatek - Uporaba ECHO
https://runcloud.io/blog/echo-command-in-linux


## Naloga 3: Naredite spremembo in jo potisnite
### Navodila:
1. Uredite obstoječo datoteko ali ustvarite novo.
2. Dodajte spremembe v območje za pripravo (staging area).
3. Commitajte spremembe.
4. Potisnite spremembe v oddaljeni repozitorij.

### Rešitev:
```sh
echo "Nekatere spremembe" >> README.md
git add README.md
git commit -m "Posodobljen README z nekaterimi spremembami"
git push
```

## Naloga 4: Ustvarite datoteko .gitignore
### Navodila:
1. Ustvarite datoteko `.gitignore` v svojem repozitoriju.
2. Dodajte vzorce datotek in imenikov, ki jih želite ignorirati.
3. Commitajte datoteko `.gitignore`.

### Rešitev:
```sh
echo "node_modules/" > .gitignore
echo "*.log" >> .gitignore
git add .gitignore
git commit -m "Dodana datoteka .gitignore"
git push
```

### Dobre prakse za .gitignore:
- Ignorirajte odvisnosti (npr. `node_modules/`).
- Ignorirajte izhodne datoteke gradnje (npr. `dist/`, `build/`).
- Ignorirajte občutljive informacije (npr. `.env`).
- Uporabite [gitignore.io](https://www.toptal.com/developers/gitignore) za ustvarjanje predlog za različne jezike in ogrodja.
