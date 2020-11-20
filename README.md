# ecolesaintmelaine

## Patch du nadir

Voir https://discuss.pixls.us/t/panography-patching-the-zenith-and-nadir/585/2

Il faut disposer de Gimp avec G'MIC.

Ouvrir l'image équi rectangulaire.
Lancer Filters > G'MIC puis Deformation > Equirectangular to nadir-zenith. Choisir Output mode à New layer

Pour le patch, on peut suivre https://geekmps.fr/tutoriaux/480-supprimer-un-objet-d-une-photo-avec-gimp-et-g-mic

Ensuite pour récupérer l'image patchée.

Sélectionner le layer
Lancer  Filters > G'MIC puis Deformation > to equirectangular. Choisir Output mode à In place

## Génération de l'output multires

Le script generate.py permet la génération des fichiers nécessaire au multires.
Il nécessite python et hugin sur la machine.

```
python generate.py -o images/multires/<dossier> <image equirectangulaire>
```

## Test en local de la visite

```
python -m SimpleHTTPServer
```

Puis ouvrir http://localhost:8000/tour.html