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
  <li>vh: altura de la pantalla visible(viewport height: 100vh)</li>
  <li>vw: anchura de la pantalla visible(viewport width: 100vw)</li>
  <li>calc(): sirve para hacer cálculos en el css al momento usando +, -, /, *.</li>
</ul>

<h3>Pseudo classes</h3>
  - <strong>hover</strong>: pasar el ratón por encima;
  - <strong>focus</strong>: se selecciona o cambia de color al darle /tab/;
  - <strong>active</strong>: al clicar en él;
  - <strong>visited</strong>: links ya visitados. Anula o escribe por encima de todos los anteriores.
  - <strong>li:first-child, li:last-child, li:nth-child(número)</strong>: para seleccionar el primer elemento, último o cualquier posición de una lista. En el último, puedo poner (even) si quiero los pares, (odd) lo impares o (3n, 4n) si los quiero de 3 en 3 o de 4 en 4, etc.
  - <strong>:not()</strong>: sirve para negar el efecto en ese elemento. P.ej: li:not(:firt-child) o h2:not(.contato)

<h3>Pseudo Elements</h3>
  - <strong>::before, ::after</strong>: añaden una decoración sin necesidad de crear un <span> en el html y evitan contaminar el doc con componentes de fines visuales. Necesitan de un /content:""/ para existir. 
  - <strong>::first-line, ::first-letter</strong>: se hacen cambios de color, tamaño, negrita, etc solo en esos elementos.