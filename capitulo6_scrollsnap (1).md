# CAPÍTULO 6: Scroll Snap y Técnicas de Scroll

## Concepto

El **Scroll Snap** es una propiedad introducida en el estándar de CSS con el objetivo de proporcionar un control más refinado sobre el desplazamiento de los elementos dentro de un contenedor. Esta técnica se basa en la capacidad de "anclar" o "encajar" los elementos de una interfaz en posiciones predeterminadas al realizar un desplazamiento horizontal o vertical. 

De acuerdo con la documentación de Mozilla Developer Network (MDN, 2022), el Scroll Snap pertenece al módulo de CSS denominado *CSS Scroll Snap Module*, el cual fue diseñado por el World Wide Web Consortium (W3C) como respuesta a la necesidad de mejorar la experiencia de desplazamiento en interfaces modernas, especialmente en dispositivos móviles donde el desplazamiento táctil es más común.  

En términos prácticos, esta característica permite que, al desplazarse sobre un contenedor que posee múltiples elementos, cada uno de ellos se alinee automáticamente con los bordes visibles de la pantalla o área del contenedor. Esto se aplica frecuentemente en carruseles de imágenes, listas horizontales, presentaciones interactivas y páginas con secciones extensas.

## Ventajas

- **Optimización de la experiencia de usuario**: facilita la navegación al asegurar que los elementos se ubiquen siempre en posiciones consistentes, reduciendo el esfuerzo visual del lector.  
- **Compatibilidad con la web responsiva**: resulta particularmente eficaz en dispositivos móviles y pantallas táctiles.  
- **Simplicidad en el desarrollo**: elimina la necesidad de scripts adicionales en JavaScript para lograr efectos de alineación en carruseles o sliders.  
- **Estandarización**: al ser una especificación de CSS, mantiene un comportamiento consistente entre navegadores modernos.  
- **Versatilidad**: puede aplicarse tanto en desplazamientos horizontales como verticales, ampliando sus posibilidades de uso.  

## Ejemplo de código

```css
/* CSS */
.container {
  scroll-snap-type: x mandatory;
  display: flex;
  overflow-x: auto;
  width: 100%;
}

.item {
  scroll-snap-align: center;
  flex: 0 0 100%;
  height: 200px;
}
```

```html
<!-- HTML -->
<div class="container">
  <div class="item" style="background: lightblue;">Sección 1</div>
  <div class="item" style="background: lightgreen;">Sección 2</div>
  <div class="item" style="background: lightcoral;">Sección 3</div>
</div>
```

## Resultado

El código anterior genera un contenedor desplazable horizontalmente en el que cada sección ocupa el 100 % del ancho de la pantalla. Al realizar scroll, los elementos se alinean automáticamente al centro del área visible, produciendo un efecto similar a un carrusel de diapositivas.

---

## Bibliografía

- Keith, J. (2020). *A complete guide to CSS Scroll Snap*. CSS-Tricks. Recuperado de https://css-tricks.com/practical-guide-to-scroll-snap/  
- Mozilla Developer Network (MDN). (2022). *CSS Scroll Snap*. Mozilla Foundation. Recuperado de https://developer.mozilla.org/es/docs/Web/CSS/CSS_Scroll_Snap  
- W3C. (2019). *CSS Scroll Snap Module Level 1*. World Wide Web Consortium. Recuperado de https://www.w3.org/TR/css-scroll-snap-1/
