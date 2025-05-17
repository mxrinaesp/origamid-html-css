# origamid-html-css

First contact with html and css

## Notes

- Shortcuts
  -ctrl a: select all
  -ctrl z: undo // ctrl shift z: go back to what I undid
  -ctrl d: multiple selection to similar
  -ctrl k c: comment code
  -ctrl b: hide side bar
  -alt + arrows: move a line up and down

- CSS: los <a>, <button>, etc no cogen el color del body en el browser pero para que lo hagan hay que poner color: inhert (hereda el color del "padre-body")

- blocks(nova linha e sozinho): <div>, <h1>, <p>...
- inline(mesma linha e nem width height margin): <a>, <span>... 
- css{ display: inline-block : o melhor das dois opções

<p> - imagens: mejor en svg (siempre hd), svg y png tienen bg transparente, no >1MB en la web </p>
<a href="https://squoosh.app/">Squoosh</a>  

- ## FLEX:
  - flex-grow: (1) elementos ocupan todo el espacio vacío del ancho (0) no lo hacen
  - flex-basis: parte del tamaño base del elemento para distribuir el espacio que sobra
  - flex-shrink: determina si un elemento puede ser menor que su tamaño original (1) puede (0) no
   * el más utilizado es flex: 1 (3 en 1 de las de arriba)

   ## POSITIONS:
   - z-index: como una montaña (fixed, relativo y absoluto)  necesita de propiedad position
   - el relativo es "absolute"a sí mismo; con el relative funcionan los top, bottom, left, right
   - absoluto SIEMPRE depende de un relativo padre (puede ser el body si no se ha especificado otro)


<ul> 
 <h3>Unidades</h3>
  <li>px</li>
  <li>rem: equivale a 16px. Es el más usado y recomendado por accesibilidad. Toma como referencia siempre la raíz, <strong>el <html>.</strong> </li>
  <li>em: no recomendado. Igual que el <strong>rem</strong>, pero toma como referente su elemento padre </li>
  <li>vh: altura de la pantalla visible(viewport height)</li>
  <li>vw: anchura de la pantalla visible(viewport width)</li>
</ul>