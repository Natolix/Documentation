---
description: Cette page va parler du système utilisé par CompagnonIA.
icon: user-robot
---

# Fonctionnement de CompagnonIA

{% hint style="warning" %}
### **Attention !**

Quelques parties peuvent contenir du code ; n'hésitez pas à appuyer sur les onglets "Explication pour les débutants" pour obtenir des informations et un codage plus simple et compréhensible pour les personnes n'étant pas avancé au codage JS.
{% endhint %}

### Les devoirs

CompagnonIA utilise un système pour déterminer quel devoir sont les plus prioritaires.

* La progression la plus avancée est sélectionnée
* Il y a des badges d'urgence, plus la date avant la date limite arrive, plus il sera prioritaire
* Quand tout est équivalent, le devoir est aléatoirement sélectionné

{% tabs fullWidth="true" %}
{% tab title="Codage" %}
{% code title="Devoirs.js" %}
```javascript
    const recommandation = devoirs
    .filter(d => !d.fait)
    .sort((a, b) => {

        // Sélectionne la progression la plus avancée
        const progA = getProgress(a);
        const progB = getProgress(b);

        if (progA !== progB) return progB - progA;

        // À cause des "badges" d'urgence, le plus urgent est sélectionné
        const urgA = getUrgencyScore(a);
        const urgB = getUrgencyScore(b);

        if (urgA !== urgB) return urgB - urgA;

        // Quand tout est équivalent, soit aucun devoir n'est affiché ou c'est aléatoire
        return Math.random() - 0.5;
    })[0];
```
{% endcode %}
{% endtab %}

{% tab title="Explication pour les débutants" %}
{% code title="Devoirs.js" lineNumbers="true" fullWidth="true" %}
```js
    const recommandation = devoirs // Fonction pour deviner quel devoir est prioritaire
    .filter(d => !d.fait) // Ne mets pas les devoirs faits
    .sort((a, b) => { // Fonction pour trier

        // Sélection par progression
        const progA = getProgress(a); // Voir la progression de A et la transformer en fonction
        const progB = getProgress(b); // Voir la progression de B et la transformer en fonction

        if (progA !== progB) return progB - progA; // Sélectionner la progression la plus avancée des devoirs

        // Sélection par badge (urgence)
        const urgA = getUrgencyScore(a); // Voir l'urgence de A et la transformer en fonction
        const urgB = getUrgencyScore(b); // Voir l'urgence de B et la transformer en fonction

        if (urgA !== urgB) return urgB - urgA; // Sélectionner l'urgence la plus haute

        // Sélection aléatoirement
        return Math.random() - 0.5; // Si tout est équivalent, chercher un devoir aléatoirement
    })[0];
```
{% endcode %}
{% endtab %}

{% tab title="Code sans explication" %}
{% hint style="info" %}
Il y a aucune explication dans ce fichier.
{% endhint %}

{% code title="Devoirs.js" lineNumbers="true" %}
```javascript
    const recommandation = devoirs
    .filter(d => !d.fait)
    .sort((a, b) => {

        const progA = getProgress(a);
        const progB = getProgress(b);

        if (progA !== progB) return progB - progA;
        
        
        const urgA = getUrgencyScore(a);
        const urgB = getUrgencyScore(b);

        if (urgA !== urgB) return urgB - urgA;

        return Math.random() - 0.5;
    })[0];
    
```
{% endcode %}
{% endtab %}
{% endtabs %}

### Les notes

Le calcul des notes, en l'occurrence la moyenne générale comme montré en dessous, c'est très simple.

{% code title="Notes.js (ce n'est pas le code)" lineNumbers="true" %}
```
Addition de toutes les notes (coef inclus) / Nombre de note
                                           ^
                                       Divisé par
```
{% endcode %}

CompagnonIA utilise un système ressemblant à cela pour pouvoir calculer les matières générales et moyennes de matières. (addition de toutes les notes d'une matière / nombre de notes)

Voici un tutoriel en 2 étapes pour trouver sa moyenne générale pondérée.

{% stepper %}
{% step %}
### Additionner toutes les moyennes des matières

Ne pas oublier de continuer les coefficients aussi. **Pour faire cela, compter deux fois la même matière pour un coefficient 2, par exemple.**
{% endstep %}

{% step %}
### Diviser le résultat par le nombre de matières

Et bam le résultat en 2 étapes simples !
{% endstep %}
{% endstepper %}
