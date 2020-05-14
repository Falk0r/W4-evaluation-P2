# Intégration d'une maquette

## Intégration d'un site web en HTML/CSS/Javascript à partir d'un pdf

Projet from scratch (partir d'une feuille blanche), le site est codé suivant la pratique __Mobile First__ qui consiste à penser la création du site en commençant par le format smartphone et d'ajouter les fonctionnalités desktop par la suite.

## Responsive

Le site est développé à partir de la technologie __Flexbox__ et de __media_queries__ assurant le coté responsive.

Le menu déroulant, lorsqu'on clique sur le "hamburger" est réalisé à l'aide d'un petit fichier javascript et du framework __Jquery__:

```Javascript
$(document).ready(function() {
    $(".fa-bars").click(function () {
        $(".menu").slideToggle("slow")
    })
})
```
et de la partie __CSS__ suivante :
```css3
ul{
    display: none;
}
.menu{
        position: absolute;
        right: 0;
        list-style: none;
        color: white;
        background-color: #1ca2f9;
        text-align: right;
        top: 50px;
        width: 100px;
        padding-right: 10px;
    }
```
sur le code __HTML__ :
```HTML
<nav>
    <i class="fas fa-bars"></i>
    <ul class="menu">
        <li><a href="#about-us">About us</a></li>
        <li><a href="#sitientis">Sitientis</a></li>
    </ul>
</nav>
```

## La touche perso en plus !
Lors d'une navigation sur smartphone, à force de dérouler la page, il est bien précieux d'avoir un bouton nous ramenant en haut de la page. Ceci nous évite de devoir remonter tout le site à la seul force de notre pouce.

Le bouton est donc implanté à l'aide de la partie __HTML__ :
```HTML
<div class="toTop">
    <a href="#top"> <i class="fas fa-chevron-circle-up"></i></a>
</div>
```
et du __CSS__ associé lui permettant d'afficher le bouton en bas à droite tout le long de la navigation :

```css3
.toTop{
        height: 40px;
        width: 40px;
        position: fixed;
        right: 10px;
        bottom: 15px;
        background-color: white;
        border-radius: 50%;
    }
    .fa-chevron-circle-up{
        color: #0298f9;
        margin: 0;
        font-size: 45px;
        margin-top: -1px;
        margin-left: -1px;
    }
```
