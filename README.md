# NMS – Transport universitaire Béjaïa (site statique)
Aucun build : Vercel sert `index.html` tel quel.

## Déployer sur Vercel
**Option 1 (sans ligne de commande)** : poussez ce dossier sur GitHub, puis vercel.com > Add New > Project > importez le dépôt.
Framework Preset : *Other*, laissez Build Command et Output Directory vides.

**Option 2 (CLI)** :

    npm i -g vercel
    cd nms-web
    vercel          # test (preview)
    vercel --prod   # production

## Données
Horaires : variable `RAW` dans index.html (transcrits depuis la photo, à vérifier).
Carte : OpenStreetMap (Leaflet). Les arrêts sont géocodés au chargement (Nominatim, mis en cache dans le navigateur) et les routes calculées par OSRM : le premier chargement peut prendre ~30 s. Pour la production, remplacez par vos coordonnées d'arrêts et un serveur de tuiles/routage dédié (les serveurs publics OSM/OSRM sont limités). Positions des bus : simulées.
