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

- CSS: los < a>, < button>, etc no cogen el color del body en el browser pero para que lo hagan hay que poner color: inhert (hereda el color del "padre-body")

- #: significa id. POR EJ.: dentro de una tag section, escribo la clase y un id=??; si en los enlaces del menú el nav he escrito #??, al princhar en él, me llevará la la section que tenía ese id.
- .: significa clase

- blocks(nova linha e sozinho): < div>, < h1>, < p>...
- inline(mesma linha e nem width height margin): < a>, < span>... 
- css display: inline-block : o melhor das dois opções

- imagens: mejor en svg (siempre hd), svg y png tienen bg transparente, no >1MB en la web
<a href="https://squoosh.app/">Squoosh</a>  

## FLEX
  - en <strong>flex-direction = row</strong>, el <em>justify-content</em> controla la distribución horizontal y el <em>align-items</em> controla la distribución vertical. En <strong>flex-direction = column</strong>, es al contrario.
  - flex-grow: (1) elementos ocupan todo el espacio vacío del ancho (0) no lo hacen
  - flex-basis: parte del tamaño base del elemento para distribuir el espacio que sobra
  - flex-shrink: determina si un elemento puede ser menor que su tamaño original (1) puede (0) no
   * el más utilizado es flex: 1 (3 en 1 de las de arriba) (los contenidos quedan del mismo tamaño)

## POSITIONS
   - z-index: como una montaña (fixed, relativo y absoluto)  necesita de propiedad position
   - el relativo es "absolute"a sí mismo; con el relative funcionan los top, bottom, left, right
   - absoluto SIEMPRE depende de un relativo padre (puede ser el body si no se ha especificado otro)

## TAGS
  En <strong>article y section</strong>, ponemos <em>aria-label="libros"</em> para que el lector accesible lea el "título" que no se muestra en la pantalla. El <em>aria-labelledby="libcom"</em>, se usa cuando el título(h1,2..) sí está en la pantalla pero no queremos que lo lea dos veces. Se coloca un <em>id="libcom"</em> después del h: < h2 id="libcom">Libros de comedia< /h2>

<ul> 
  <h3>Unidades</h3>
  <li>px</li>
  <li>rem: equivale a 16px. Es el más usado y recomendado por accesibilidad. Toma como referencia siempre la raíz, <strong>el < html>.</strong> </li>
  <li>em: no recomendado. Igual que el <strong>rem</strong>, pero toma como referente su elemento padre </li>
  <li>vh: altura de la pantalla visible(viewport height: 100vh)</li>
  <li>vw: anchura de la pantalla visible(viewport width: 100vw)</li>
  <li>calc(): sirve para hacer cálculos en el css al momento usando +, -, /, *.</li>
</ul>

<ul>
  <h3>Pseudo classes</h3>
  <li><strong>hover</strong>: pasar el ratón por encima;</li>
  <li><strong>focus</strong>: se selecciona o cambia de color al darle /tab/;</li>
  <li><strong>active</strong>: al clicar en él;</li>
  <li><strong>visited</strong>: links ya visitados. Anula o escribe por encima de todos los anteriores.</li>
  <li><strong>li:first-child, li:last-child, li:nth-child(número)</strong>: para seleccionar el primer elemento, último o cualquier posición de una lista. En el último, puedo poner (even) si quiero los pares, (odd) lo impares o (3n, 4n) si los quiero de 3 en 3 o de 4 en 4, etc.</li>
  <li><strong>:not()</strong>: sirve para negar el efecto en ese elemento. P.ej: li:not(:firt-child) o h2:not(.contato)</li>
</ul>

<ul>
  <h3>Pseudo Elements</h3>
  <li><strong>::before, ::after</strong>: añaden una decoración sin necesidad de crear un <span> en el html y evitan contaminar el doc con componentes de fines visuales. Necesitan de un /content:""/ para existir. Son un elemento diferente, son position absolute del padre relative.</li>
  <li><strong>::first-line, ::first-letter</strong>: se hacen cambios de color, tamaño, negrita, etc solo en esos elementos.</li>
</ul>

## RESPONSIVO
  <ul>
    <li>Poner la meta tag de viewport en el head, SI NO, NO FUNCIONA LA VERSIÓN MÓVIL.</li>
    <li>medida img max-width: 100%. Poner % hace que sea responsivo</li>
    <li>@media (max-width: 600px) {} significa que todo lo que ponga entre los corchetes se va a aplicar cuando la pantalla sea menor de 600px. </li>
    <li>@media (min-width: 700px) and (max-width: 900px), va a aplicar  estilo sólo cuando la pantalla esté entre 700 y 900px.</li>
    <li>@media screen/print aplica los estilos solo en la pantalla o solo a la hora de imprimir.</li>
    <li>la parte responsiva "@media (...) {}" poner al final del css para que no sea ignorada cuando se defina el style del sitio </li>
    <li>object-fit: cover. Sirve para que la imagen se adapte al texto, y en vez de estirarse, hace "zoom". <strong>Solo usarlo si la imagen tiene sentido cortada.</strong></li>
    <li>object-position: top right. El "zoom" coge la parte de arriba de la derecha de la foto.</li>
    <li>medida bloque de texto: ch. Si ponemos <em>max-width:60ch</em>, significa que cada línea del texto se extenderá de ancho lo mismo que ocuparían 60 "0"s, sin importar los píxeles de la pantalla, su tamaño, etc.</li>
    <li>con <strong>word-break: break-all</strong>, que rompe la palabra y el bloque de texto coge la anchura deseada sin que quede feo.</li>
  </ul>

## PROYECTO PORTFOLIO
  <ul>Header
    <li>cuando tenemos un max-width, el <em>margin: 0 auto</em> da márgenes laterales automáticos y proporcionales, simulando un autocentralizado en el elemento (en este caso el header).</li>
  </ul>

  <ul>Introdução
    <li>< br> sirve para romper una palabra en una p o h1.</li>
  </ul>

  <ul>Formação
    <li>! important hace que cualquier elemento sea más importante que el resto, sin importar su orden.</li>
    <li>en el responsive, si los iconos se me cortan, cambio de position absolute a initial y se ponen encima del h3.</li>
  </ul>

  Usar <strong>Lighthouse</strong> en "inspeccionar" para optimizar la página web.

## LÍNEA DE COMANDO (TERMINAL)
  - <strong>ls</strong>: enumera los elementos (carpetas y archivos) que hay dentro de lo morado.
  - <strong>cd + nombre_carpeta</strong>: entra dentro de esa carpeta.
  - <strong>cd ..</strong>: sube a la carpeta de arriba.
  - <strong>mkdir + nombre_carpeta</strong>: crea una carpeta nueva.
  - <strong>touch + nombre_archivo.extensión</strong>: crea un archivo .css, .html, .js, etc.
  - <strong>touch nombre_carpeta/nombre_archivo.extensión</strong>: crea un archivo dentro de una carpeta (e.j: touch css/style.css).
  - <strong>rm nombre_archivo.extensión</strong>: elimina un archivo. ¡MUCHO CUIDADO!
  - <strong>rm -r nombre_carpeta</strong>: elimina una carpeta.

  <h2>NPM y CleanCSS</h2>
  - cleancss -o nombre_archivo.min.extensión nombre_archivo.extensión (ej: cleancss -o style.min.css style.css): sirve para quitarle peso al archivo al subirlo a la web. !! IMPORTANTE CAMBIARLO EN LA META TAG DEL HTML.

  <h2>GIT</h2>
  - cuando creo un repositorio en github, tiene que ser mi user + .github.io (ej: mxrinaesp.github.io)
  <ul>
    <li>git add -A: añade todos los archivos al repositorio</li>
  </ul>

## FORMULARIOS
  - la tag < form> incluye un action="url" y un method="get/post".
  - < input type="" id="" name="" required placeholder="xxx-xx-xx-xx" disabled>
  - < label for="" >< /label>
  - < button>Enviar< /button>. Se puede modificar todo el CSS. !!cursor: pointer!! para que aparezca la manita y se vea que es elemento clicable.
  - dentro va el campo <strong>< input type="text"></strong>. Es un campo solo de apertura.
  - dentro va tb el <strong>< label for=""></strong> escribimos aquí el título o etiqueta del formulario.
  - el <strong>for=""</strong> del label tendrá el mismo nombre que el <strong>id=""</strong> del input. Esto hace que al clickar en la palabra del label, se pueda escribir directamente en el input text.
  - después de id="" en el input, ponemos <strong>name=""</strong>, que será la palabra que aparece en el link de la página después de darle al botón de enviar. NORMALMENTE EL FOR="", ID="" Y NAME="" TIENEN EL MISMO NOMBRE.
  - el <strong>input type="password"</strong> hace que se vea con puntitos aunque no está oculto porque se verá en la url con el name.
  - si escribo <em>required</em> en el input, saltará un pop-up obligando a rellenar el campo.
  - el <strong>input type="number"</strong> solo deja escribir números.
  - el <strong>input type="date"</strong> sirve para poner fechas.
  - el <strong>input type="checkbox"</strong> sirve para marcar una cajita con un tick. Si pongo value="aceito",
  en la url aparecerá =aceito si está on. Permite seleccionar varios.
  - el <strong>input type="radio"</strong> marca un circulito. Solo permite seleccionar uno u otro.
  - si escribo <em>placeholder=""</em> en el input, dará una idea de cómo rellenar el campo. P.ej: xxx-xx-xx-xx sería el formato en que escribir el nº de tlf.
  - si escribo <em>disabled</em> en el input, se deshabilita el campo.
  -
  - la tag < select> incluye name="" y id="". Sería otra variante de <em>input</em>. Dentro de ella se colocan opciones de selección. Va junto con < label>.
  - las opciones van dentro de la tag < option>, con un value="" que será lo que aparezca en la url.
  - 
  - la tag < textarea> incluye name="", id="", cols="" y rows="". Permite escribir un párrafo. Va junto con < label>.
  Las cols apenas se usan; las rows indican cuántas líneas visibles hay en la caja, pero se pueden escribir más.

## SELECTORES EN CSS
 ### Atributos
  - Selecciona solo los elementos cuyo atributo esté entre corchetes. p.ej: [ required]
  - Selecciona solo el elemento que tenga el atributo y el valor. p.ej: [ name="recogida"] 
  - Atributos que empiecen <strong>^</strong> con el valor. p.ej: [ href^="#"]
  - Atributos que terminen <strong>$</strong> con el valor. p.ej: [ href$=".com"]

 ### Signos
  -> : p.ej: div > p... solo el p que es hijo directo de div.
  -+: p.ej: p + p... todo p que venga después de un p. 
  -*: selecciona todos los elementos del site.