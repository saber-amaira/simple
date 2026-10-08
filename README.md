# Inscription enfant

Site statique d'une seule page : un formulaire d'inscription pour un enfant, dessiné comme une page de cahier à grands carreaux.

```
public/index.html   la page (HTML, CSS et JS dans un seul fichier)
render.yaml         configuration du site statique sur Render
```

## Avant de publier

1. **Relier le formulaire.** Un site statique ne peut pas recevoir de données seul. Créez un formulaire chez un service de réception (par exemple [Formspree](https://formspree.io)), puis collez son adresse dans `public/index.html` :

   ```js
   const FORM_ENDPOINT = "https://formspree.io/f/xxxxxxxx";
   ```

   Tant que cette ligne est vide, la page affiche « Le formulaire n'est pas encore relié… » et n'envoie rien.

2. **Personnaliser les textes.** Nom de la structure (« Le Petit Cahier »), année de rentrée, liste des classes, et phrase du bas de page (ajoutez-y votre adresse email de contact).

## Publier sur Render

1. Sur [dashboard.render.com](https://dashboard.render.com), choisir **New → Blueprint** et sélectionner ce dépôt (Render lit `render.yaml`).
2. Valider : le site est en ligne sur une adresse en `onrender.com` à chaque push sur `main`.

Sans Blueprint : **New → Static Site**, dépôt `saber-amaira/simple`, *Publish directory* = `public`, commande de build vide.

## Données personnelles

Le formulaire collecte des données sur des mineurs, dont des informations de santé. Avant la mise en ligne publique, vérifiez que le service de réception choisi convient (hébergement, durée de conservation) et ajoutez vos mentions légales.
