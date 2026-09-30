---
description: Cette page décri le fonctionnement de la messagerie de Compagnon
icon: gears
---

# Fonctionnement de la messagerie

{% hint style="warning" %}
#### Attention !

Comparé à une page précédente, le codage ne sera pas résumé. Cette page contient du codage JavaScript.
{% endhint %}

## Étapes pour recevoir le message

{% stepper %}
{% step %}
### **Obtenir le message de la part de Zimbra (messagerie MBN)**

**Zimbra** est la messagerie utilisée par MBN (Mon Bureau Numérique), grâce à sa fonction qui lui permet d'exporter les mails ; un automatisme est utilisé pour exporter les nouveaux mails pour ensuite les convertir en code, et les afficher.
{% endstep %}

{% step %}
### Automatiquement exporter le message

_Plus d'explications ci-dessus._
{% endstep %}

{% step %}
### Le transformer en code et l'afficher

Le code ressemble à ceci dès que le mail est complètement déchiffré.

```
{
  id: 10000,
  sender: "Documentation",
  email: "docs@compagnon.app",
  subject: "Bienvenue !",
  content: `Bienvenue sur la messagerie Compagnon !`
},
```

**id:** L'ordre auquel affiche le message (l'ID est directement dans le nom du fichier exporté, ce qui est plus simple pour trier par date).

**sender:** La personne ayant envoyé le message

**email:** Le mail de la personne ayant envoyé le message

**subject:** Le titre du message

**content:** Le contenu du message

**unread (optionnel):** Afficher (ou non) si le message a été lu

**date (optionnel):** Afficher la date de publication du message

**badge (optionnel):** Mets "Officiel", "Annonce", "Interne" ou "Externe"

Basé sur le code ci-dessus. Voici à quoi ressemble la messagerie.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Affichage de la page Messagerie avec le code mis au-dessus</p></figcaption></figure></div>
{% endstep %}
{% endstepper %}
