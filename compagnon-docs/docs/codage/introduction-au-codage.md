---
description: Démarrons tranquillement avec les introductions au codage
icon: '1'
tags:
  - page-a-jour
---

# Introduction au codage

## Création du projet

Pour pouvoir commencer à créer une application du style de Compagnon, il faut bien évidemment avoir les applications nécessaires.

<table data-view="cards"><thead><tr><th></th><th data-hidden data-card-cover data-type="image">Cover image</th></tr></thead><tbody><tr><td>Android Studio (<a href="https://developer.android.com/studio">https://developer.android.com/studio</a>)</td><td><a href="../.gitbook/assets/image.png">image.png</a></td></tr><tr><td>npm (<a href="https://npmjs.com/">https://npmjs.com</a>)</td><td><a href="https://studio.uxpincdn.com/studio/wp-content/uploads/2022/04/logo-uxpin-merge-npm-packages.png.webp">https://studio.uxpincdn.com/studio/wp-content/uploads/2022/04/logo-uxpin-merge-npm-packages.png.webp</a></td></tr><tr><td>Figma (<a href="https://figma.com/">https://figma.com</a>)</td><td><a href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS_eY3w3QxxVMh9noG8aVaKqIoRyYDSpuNmww&#x26;s">https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS_eY3w3QxxVMh9noG8aVaKqIoRyYDSpuNmww&#x26;s</a></td></tr><tr><td>Visual Studio Code (<a href="https://code.visualstudio.com/">https://code.visualstudio.com</a>)</td><td><a href="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/500px-Visual_Studio_Code_1.35_icon.svg.png">https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/500px-Visual_Studio_Code_1.35_icon.svg.png</a></td></tr><tr><td>Papillon (<a href="https://docs.papillon.bzh/">https://docs.papillon.bzh</a>) qui est <strong>très utile</strong> avec sa large documentation</td><td><a href="https://cdn.aptoide.com/imgs/1/c/e/1ce74d86f002dda431724a60ba11e7d7_fgraphic.png">https://cdn.aptoide.com/imgs/1/c/e/1ce74d86f002dda431724a60ba11e7d7_fgraphic.png</a></td></tr><tr><td>Git (<a href="https://git-scm.com/">https://git-scm.com</a>)</td><td><a href="https://docs.papillon.bzh/~gitbook/image?url=https%3A%2F%2F4251740737-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLt8mMBbf7ntjxrd29I4o%252Fuploads%252Fgit-blob-7aa31b6bd3c8610e4aaf66a9ad2871bd949b3d56%252Fgit.jpg%3Falt%3Dmedia&#x26;width=245&#x26;dpr=2&#x26;quality=100&#x26;sign=54ae8d5c&#x26;sv=2">https://docs.papillon.bzh/~gitbook/image?url=https%3A%2F%2F4251740737-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FLt8mMBbf7ntjxrd29I4o%252Fuploads%252Fgit-blob-7aa31b6bd3c8610e4aaf66a9ad2871bd949b3d56%252Fgit.jpg%3Falt%3Dmedia&#x26;width=245&#x26;dpr=2&#x26;quality=100&#x26;sign=54ae8d5c&#x26;sv=2</a></td></tr></tbody></table>

{% hint style="info" %}
Certaines applications ci-dessus ne sont pas nécessaires, mais recommendés.
{% endhint %}

### Cloner Compagnon

Dès que **Git** est installé, il faut le lancer et faire la commande suivante dans l'application :&#x20;

```git-commit
$ git clone https://github.com/AppCompagnon/Compagnon.git
```

Dès que cela est fait, il faut faire les commandes suivantes :&#x20;

{% tabs %}
{% tab title="Windows" %}
```git-commit
$ cd Compagnon
$ npm install
$ npx expo prebuild
```
{% endtab %}

{% tab title="MacOS" %}
```git-commit
$ cd Compagnon
$ npm install
$ npx expo prebuild
$ cd ios && pod install && cd ../
```
{% endtab %}
{% endtabs %}

C'est fini ! Pour pouvoir le lancer, il faut :&#x20;

{% tabs %}
{% tab title="Android" %}
```git-commit
$ npm run android
```
{% endtab %}

{% tab title="iOS/iPadOS" %}
{% hint style="danger" %}
Un Mac est requis pour pouvoir lancer une session iOS ou iPadOS
{% endhint %}

```git-commit
$ npm run ios
```
{% endtab %}
{% endtabs %}
