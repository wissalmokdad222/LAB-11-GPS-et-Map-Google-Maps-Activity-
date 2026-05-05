# Projet Android Google Maps

##  Pourquoi la carte ne s'affiche pas ?

Si vous lancez l'application et que vous voyez un écran vide ou une grille sans routes

![](https://github.com/user-attachments/assets/ebb07d46-c403-47f4-bbf6-943cd4f453dc)

c'est probablement dû à l'absence d'une clé API valide ou à la configuration de facturation Google Cloud.

![](https://github.com/user-attachments/assets/52d82451-b9d9-42b9-a394-e73dc48ddfad)

![](https://github.com/user-attachments/assets/a7317035-2348-470f-9b26-19b750faab33)
### 1. La clé API est obligatoire
Pour utiliser le SDK Google Maps, vous devez générer une clé API sur la [Console Google Cloud](https://console.cloud.google.com/). 
Cette clé doit être placée dans le fichier :
`app/src/main/res/values/google_maps_api.xml`

### 2. Le service est "payant" (Billing)
Depuis quelques années, Google impose d'associer un **compte de facturation (carte bancaire)** à votre projet Google Cloud pour activer Maps, même pour le développement.
![](https://github.com/user-attachments/assets/775a6fe9-dd23-4207-9227-191bff51967d)
**Important à savoir :**
* **Crédit Gratuit :** Google offre environ **200$ de crédit chaque mois**, ce qui couvre largement l'utilisation pour l'apprentissage et les tests (gratuit en pratique pour ce projet).
* **Sécurité :** Sans compte de facturation actif, Google bloque l'affichage des tuiles de la carte.

## Configuration requise
1. Créer un projet sur Google Cloud Console.
2. Activer le **Maps SDK for Android**.
   ![](https://github.com/user-attachments/assets/b6db12b0-824f-4bbf-8aa4-23d27314eb42)
4. Associer un compte de facturation .
5. Créer une clé API et la restreindre à votre application avec le SHA-1 :
   `EA:49:79:2A:CD:94:C6:C2:D4:DE:46:95:B6:42:0D:8E:E6:24:24:E0`
6. Coller la clé dans `google_maps_api.xml`.
