# 📅 Setup Calendly (10 min, gratuit)

Le widget Calendly est déjà intégré dans `studio-photo.html`. Il te reste juste à créer ton compte Calendly et configurer le créneau "20 min appel découverte". Tu peux ensuite remplacer le slug dans le HTML si nécessaire.

## 1. Créer ton compte Calendly

Va sur **https://calendly.com/signup** et crée un compte (gratuit, plan "Basic" largement suffisant).

- **Email** : `evanorofino.pro@gmail.com`
- **Slug Calendly** : choisis `evanorofino-pro` (= URL `calendly.com/evanorofino-pro`)
- **Connecte Google Calendar** pour synchroniser tes dispos en temps réel

## 2. Créer le type d'événement "20 min appel découverte"

Dans Calendly :
1. Clique **+ Create** → **Event Type**
2. Type : **One-on-One**
3. Configure :
   - **Name** : `Appel découverte Studio Photo`
   - **Description** : "Démo de la plateforme + échange sur votre projet photo. 20 minutes, sans engagement, en visio (Google Meet auto)."
   - **Location** : Google Meet (auto-lien généré à chaque RDV)
   - **Duration** : **20 minutes**
   - **Event link** : `20min` → URL finale `calendly.com/evanorofino-pro/20min`
4. **Date range** : "Indefinitely into the future" (toujours dispo)
5. **Buffer time** : 15 min avant + 15 min après (pour respirer entre 2 RDV)
6. **Daily limit** : 5 max par jour
7. **Booking notice** : 4 heures min (évite les RDV de dernière minute)

## 3. Personnaliser les questions au prospect

Onglet **Invitee Questions** → ajoute :
- **Question 1** : "Quel type de photos faites-vous principalement ?" (mariage / portrait / corporate / événementiel / autre)
- **Question 2** : "Avez-vous déjà un site web ? Si oui, lequel ?" (URL libre)
- **Question 3** : "Quel est votre principal point de douleur aujourd'hui ?" (réponse longue, optionnelle)

→ Ça te donne le contexte avant l'appel, tu arrives préparé.

## 4. Vérifier l'intégration dans studio-photo.html

Le widget est déjà en place dans `studio-photo.html` (section `#calendly`) :

```html
<div class="calendly-inline-widget"
     data-url="https://calendly.com/evanorofino-pro/20min?primary_color=c8a97e"
     style="min-width:320px; height:680px;"></div>
<script type="text/javascript" src="https://assets.calendly.com/assets/external/widget.js" async></script>
```

Si tu as choisi un slug Calendly différent (ex : `evan-orofino`), édite le `data-url`.

## 5. Tester

1. Ouvre https://evanorofino.github.io/portfolio/studio-photo.html (après le prochain push)
2. Scrolle jusqu'à "Réservez 20 min, je vous montre la démo"
3. Choisis un créneau, valide → tu dois recevoir l'email de confirmation Calendly
4. Va dans Calendar → tu vois le RDV automatiquement créé

## 6. Notifications

Active dans Calendly :
- ✅ Email à toi pour chaque nouveau RDV
- ✅ Email de rappel 1h avant au prospect
- ✅ SMS de rappel 1h avant (plan Premium, $10/mois — pas nécessaire pour démarrer)

## 7. Page de remerciement personnalisée

Calendly → **Confirmation page** → **Display custom redirect** :
- URL : `https://evanorofino.github.io/portfolio/studio-photo.html#thanks`
- (Optionnel) Ajoute une ancre `#thanks` dans le HTML avec un message "Merci ! Vérifie ton email."

## 💡 Bonus : Branding gold/black

Dans **Account settings** → **Branding** :
- **Primary color** : `#c8a97e` (gold Studio Photo)
- **Logo** : upload un mini-logo (256×256 PNG)
- **Background** : `#1a1a1a` ou laisser blanc

---

✅ **Une fois Calendly configuré et le slug à jour**, ton lien magique à envoyer en LinkedIn devient :

> https://evanorofino.github.io/portfolio/studio-photo.html#calendly

Le prospect clique → arrive directement sur ton calendrier de RDV → réserve en 30 secondes → tu reçois la notif sur ton tél. **Cycle de vente raccourci de 3-4 jours à 30 secondes.**
