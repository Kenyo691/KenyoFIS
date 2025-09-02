# CAPÍTULO 7: Clipping y Masking con CSS

## Concepto

Dentro de las técnicas avanzadas de diseño web, el **Clipping** y el **Masking** en CSS representan recursos fundamentales para la manipulación visual de los elementos. Ambas técnicas tienen como finalidad alterar las áreas visibles de un elemento, aunque lo hacen mediante mecanismos distintos:

- **Clipping**: se basa en la utilización de la propiedad `clip-path`, la cual permite definir una región geométrica (círculos, elipses, polígonos, entre otros) que delimita la parte del elemento que será visible. El contenido fuera de la forma definida se oculta sin modificar realmente el DOM.  
- **Masking**: emplea una imagen o un gradiente como máscara mediante la propiedad `mask-image` (o `-webkit-mask-image` en algunos navegadores). La máscara determina qué partes del elemento serán visibles en función de la opacidad o transparencia de la imagen aplicada.  

Según Coyier (2021), estas herramientas amplían considerablemente la creatividad del diseñador, dado que permiten crear interfaces más dinámicas, con efectos visuales modernos sin necesidad de editar previamente las imágenes en un software externo.

## Ventajas

- **Mayor expresividad visual**: posibilitan el uso de formas y patrones personalizados que enriquecen el diseño de interfaces.  
- **Flexibilidad**: mientras el clipping se orienta a recortes geométricos, el masking admite imágenes complejas y gradientes.  
- **Optimización de recursos**: evita la necesidad de generar imágenes editadas previamente, ya que los efectos se logran directamente con código.  
- **Compatibilidad moderna**: ampliamente soportado en navegadores actuales, aunque en algunos casos se requiere prefijos específicos.  
- **Aplicaciones dinámicas**: se pueden integrar con transiciones y animaciones para efectos interactivos en páginas web.  

## Ejemplo de código

```css
/* CSS */
.clipped {
  width: 300px;
  height: 300px;
  background: url('https://picsum.photos/400') no-repeat center/cover;
  clip-path: circle(50% at 50% 50%);
}

.masked {
  width: 300px;
  height: 300px;
  background: url('https://picsum.photos/400') no-repeat center/cover;
  -webkit-mask-image: linear-gradient(to bottom, black 70%, transparent 100%);
  -webkit-mask-repeat: no-repeat;
  -webkit-mask-size: cover;
}
```

```html
<!-- HTML -->
<div class="clipped"></div>
<br>
<div class="masked"></div>
```

## Resultado

El primer ejemplo aplica un recorte circular a la imagen de fondo del elemento, mostrándola como si estuviera contenida en un círculo perfecto. El segundo ejemplo utiliza un degradado como máscara, de modo que la parte inferior de la imagen se desvanece progresivamente hasta volverse transparente.

---

## Bibliografía

- Coyier, C. (2021). *Clipping and Masking in CSS*. CSS-Tricks. Recuperado de https://css-tricks.com/clipping-masking-css/  
- Meyer, E. A. (2018). *CSS: The Definitive Guide* (4.ª ed.). O’Reilly Media.  
- Mozilla Developer Network (MDN). (2022). *clip-path*. Mozilla Foundation. Recuperado de https://developer.mozilla.org/es/docs/Web/CSS/clip-path  
- Mozilla Developer Network (MDN). (2022). *mask-image*. Mozilla Foundation. Recuperado de https://developer.mozilla.org/es/docs/Web/CSS/mask-image
