
# Frontend Mentor - Blog preview card solution 

This is my solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). A simple proyect to consolidate my most basic skills with css. I hope you enjoy it.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I have learned](#What-I-have-learned)
- [Author](#author)


## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./images/screenshot.jpg)


### Links

- Solution URL: [https://franciscomi.github.io/blog-preview-card-main/]


## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties

### What I have learned

- Trabajar con unidades de medida en CSS (Diferencias entre <b>em</b> y <b>rem</b>)

  'em' es una unidad relativa de CSS que se basa en el tamaño de la fuente del elemento padre. 
  
  En nuestro caso hemos establecido el tamaño del elemento <body> de HTML en 16px. <body> inicialmente sería '1em'. Si ponemos '0.5em' sería la mitad del tamaño de la fuente. Esto es igual para otras propiedades como 'margin' o 'padding'.

  ```css
  /*Elemento padre*/
  body{
    font-size:16px
  }

  /*Elemento hijo*/
  div{
    font-size:0.5em; /*Serían 8px*/
    margin-left:1em; /*El margen derecho de la caja es de 16px*/
  }
  ```

  'rem' es similar a 'em', pero con la diferencia de que en lugar de ser relativo al tamaño de fuente de un elemento padre, es relativo al tamaño de la fuente raíz (normalmente el <html> o el <body>).

  ```css
  div{
    font-size:0.5rem;
    margin-left:1rem;
  }
  ```


- Usar la función 'clamp()' en css para escalar los elementos de la web

  'clamp()' en css nos permite establecer un rango de valores posibles a un elemento HTML. La sintáxis es la siguiente:
  ```css
  property: clamp(min, ideal, max);
  ```
  En nuestro caso queremos mantener el tamaño de letra de nuestra tarjeta, que ha sido establecido en 16px siendo 16px=1rem, entre un mínimo de 8px y un máximo de 16px, siendo el ideal el que depende del tamaño del ancho de la página.

  ```css
  .card{
    font-size: clamp(0.50rem, 1.5vw + 0.5rem, 1rem); 
  }
  ```

## Author

- Website - [https://franciscomi.github.io/blog-preview-card-main/]
- Frontend Mentor - [@FranciscoMi](https://www.frontendmentor.io/profile/FranciscoMi)
