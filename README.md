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

- #: significa id. POR EJ.: dentro de una tag "section", escribo la clase y un id=??; si en los enlaces del menú el nav he escrito #??, al princhar en él, me llevará a la section que tenía ese id.
- .: significa clase

- blocks(nova linha e sozinho): < div>, < h1>, < p>. < img>...
- inline(mesma linha e nem width height margin): < a>, < span>... 
- css display: inline-block : o melhor das dois opções (a)

- imagens: mejor en svg (siempre hd), svg y png tienen bg transparente, no >1MB en la web
<a href="https://squoosh.app/">Squoosh</a>  

## FLEX
  - en <strong>flex-direction = row</strong>, el <em>justify-content</em> controla la distribución horizontal y el <em>align-items</em> controla la distribución vertical. En <strong>flex-direction = column</strong>, es al contrario.
  - flex-grow: (1) elementos ocupan todo el espacio vacío del ancho (0) no lo hacen.
  - flex-basis: parte del tamaño base del elemento para distribuir el espacio que sobra.
  - flex-shrink: determina si un elemento puede ser menor que su tamaño original (1) puede (0) no.
   * el más utilizado es flex: 1 (3 en 1 de las de arriba) (los contenidos quedan del mismo tamaño *
  - flex-wrap: wrap -> permite que los elementos se reorganicen en la pantalla cuando la hago más pequeña, en vez de desaparecer.

## POSITIONS
   - z-index: como una montaña (fixed, relativo y absoluto) necesita de propiedad position.
   - el relativo es "absolute" a sí mismo; con el relative funcionan los top, bottom, left, right.
   - absoluto SIEMPRE depende de un relativo padre (será el body si no se ha especificado otro).

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
    <li>poner la meta tag de viewport en el head. SI NO, NO FUNCIONA LA VERSIÓN MÓVIL.</li>
    <li>medida img max-width: 100%. Poner % hace que sea responsivo</li>
    <li>@media (max-width: 600px) {} significa que todo lo que ponga entre los corchetes se va a aplicar cuando la pantalla sea menor de 600px. </li>
    <li>@media (min-width: 700px) and (max-width: 900px), va a aplicar estilo sólo cuando la pantalla esté entre 700 y 900px.</li>
    <li>@media screen/print aplica los estilos solo en la pantalla o solo a la hora de imprimir.</li>
    <li>la parte responsiva "@media (...) {}" poner al final del css para que no sea ignorada cuando se defina el style del sitio </li>
    <li>object-fit: cover. Sirve para que la imagen se adapte al texto, y en vez de estirarse, hace "zoom". <strong>Solo usarlo si la imagen tiene sentido cortada.</strong></li>
    <li>object-position: top right. El "zoom" coge la parte de arriba de la derecha de la foto.</li>
    <li>medida bloque de texto: ch. Si ponemos <em>max-width:60ch</em>, significa que cada línea del texto se extenderá de ancho lo mismo que ocuparían 60 "0"s, sin importar los píxeles de la pantalla, su tamaño, etc.</li>
    <li>con <strong>word-break: break-all</strong>, que rompe la palabra y el bloque de texto coge la anchura deseada sin que quede feo.</li>
  </ul>

## PROYECTO PORTFOLIO LOBO
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
  - Para arreglar un fallo en el mensaje del commit: <strong>git commit --amend</strong>, ctrl o, ctrl x.
  Si ya hice push, después del amend: <strong>git push -f</strong>

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
  - +: p.ej: p1 + p... todo p que venga después de un p1. (solo el siguiente hermano adyacente)
  - *: selecciona todos los elementos del site.

## PROPIEDADES CUSTOMIZADAS
  - <strong>--verde: #caf;  var(--verde);</strong>: sirve para reutilizar una propiedad (un color, un borde específico, un tamaño de letra...). La primera parte se escribe en el html o en el <strong>:root</strong>, y la segunda es una función para escribir en cualquier tag donde quiera reutilizar esa propiedad (p.e: color: var(--verde);).
  ### Dark&Light Mode
  - @media (prefers-color-scheme: light/dark): las propiedades que creo solo se usarán cuanso el sistema/navegador esté en modo claro/oscuro.
  - <em>Es mejor poner el :root como predeterminado al principio y luego crear el @media con dark; así el tema padrón será el root a no ser que el usuario tenga activado el dark mode.</em>

## CSS UTILITARIO
  - Consiste en crear clases con propiedades predefinidas para escribir en el HTML.
  - <em>Bootstrap</em> no necesita de CSS porque sus clases ya incluyen los valores.

-----------------------------------------------------------------------------------------
## PROYECTO FINAL
  - al principio del CSS:
      - dejar en margin: 0 el body, p, h1, ul...;
      - establecer la font-family del body;
      - list-style: none y padding: 0 de los ul;
      - text-decoration: none y color: inherit de los a;
      - max-width: 100% y display: block de los img;
    
  - box-sizing: border-box -> el padding y el border no aumentan el tamaño total del elemento, sino que se restan del ancho y alto especificados.
  - transition: 0.3s.
  - margin-bottom: usar siempre cuando haya varios elementos en columna en vez de mezclar m-t, padding, etc.
  - box-shadow: 0px 0px 0px #fff -> lado, abajo, borroso, color.
  - transform: translateX(2px) -> cuando hay un icono en el botón y queremos que se "traslade" 2px a la derecha al hacer hover.
  
  - la introducción va dentro de una tag main.
  - cuando la introducción o lo que sea tiene texto a un lado e img al otro, meter texto e img en divs diferentes. La imagen tiene que tener height y width:100%; object-fit: cover.
  - si quiero crear una ilusión de que la foto "sobresale" del container, es poner un box-shadow: inset 0 +/-120px white en x-bg y ajustar el padding-bottom o top en x-conteudo. O también en el bg poner background: linear-gradient (to right, white 30%, black 30%).

  - en el CSS utilitario: para la tipografía, puedo escribir font: weight size/line-height "family" (p.ej: font: 600 4rem/1.125 "Poppins")

  - en la bicicletas-lista debajo de la intro, para que el h2 de ambas partes se mantenga alineado, coloco mismo max-width(1200px) y margin auto!!; si coloco padding, recordar el border-box para que mantenga los 1200px.
  - si quiero un scroll en solo un apartado del site, p. ej, en una lista de bicicletas: dentro de la ul, <strong>overflow-x: auto</strong> permite hacer scroll hacia el lado y ver las 3 fotos (antes hemos puesto min-width en el li para que las fotos sean grandes)
  - <em>si quiero poner margin, padding, etc en un span -> ponerlo en display block</em>.
  - colocar <strong>width: max-content</strong> para que el h3 de la tecnologia-vantagens no quebre al disminuir patalla.

  - en nossos parceiros, la <em>ul</em> es un grid porque son varias columnas. Pero cada <em>li</em> es un flex para poder dejar las img con margin auto y que queden alineadas.
  - para hacer una cuadrícula y quitar los border exteriores: li:nth-child(n + 0) y border-left/top.

  - en el footer: en un enlace <em>a</em>, puedo poner href="tel:+xx xxxxx" o href="mailto:aaaa@aaa.aa" y me lleva directamente al clickar a la app del tlf o la del correo.

  - <strong>RESPONSIVO SIN MEDIA QUERY:</strong> en la ul de seguros/vantagens.css, en el <em>grid-template-columns</em>, en vez de poner 1fr 1fr 1fr; pongo <em>: repeat(auto-fit, minmax(280px-p.ej-, max-content))</em>. De esta manera, según el ancho de la página, se crearán automáticamente 3, 2 o 1 columna.

  - si tengo una div de 3 imágenes y quiero que se pongan en triángulo (1 arriba y 2 abajo), tengo que hacer un <em>display:flex</em> del padre con flex-wrap; luego mencionar al padre y a las img (p-ej: .bicicleta-imagens img {}) con <em>flex:1 y min-width de 200px</em>; y por último, img:first-child <em>min-width: 100%</em>.

  - Cuando tengo enlaces (como en la parte de contato: email, tlf, etc), mejor poner display: block pq si pongo inline-block, al aumentar el width de la página, se va a poner al lado en vez de uno encima de otro. También poner max-width: max-content para que solo puedan clickar encima del enlace.

  -<strong>BLOQUE CON VISIBILIDAD ALTERNADA SIN JAVASCRIPT ACTIVADO CON INPUT RADIO</strong> Primero creo dos inputs type=radio y dos bloques(div) con los respectivos ids: input#bikcraft, input#seguro,div#orcamento-bikcraft y div#orcamento-seguro. Estilizo los bloques por defecto con display: none; y entonces creo un estilo condicional para cada bloque con su input :checked ~ respectivo agregando el display: block; Por ejemplo: <em>#bikcraft:checked ~ #orcamento-bikcraft { display: block; }</em>  

  - cuando quiero estilizar un input, tengo que especificar su tipo. P.ej.: .orcamento-produto input[type="text"]

-----------------------------------------------------------------------------------------------

# JAVASCRIPT BÁSICO
 - <strong>console.log('nombre_variable')</strong>
 - <strong>console.dir(nombre_variable)</strong>: me enseña todas las propiedades y métodos de esa variable
 - variables utilizadas: <strong>const</strong> y <strong>let</strong>;
    <em>const</em>: es sensitive case; empezar siempre con letra, no con nº; usar underline para separar; solo un valor para una constante (el primero). Por ej.: const Nome = "JavaScript"; -- Nome = "Teste"; -- console.log(Nome); va a aparecer JavaScript en el Console.
    <em>let</em>: igual solo que sí puedo reescribir por ej.: let Nome = "JavaScript"; -- Nome = "Teste"; -- console.log(Nome); -- y aparecerá Teste porque es el último escrito.

    Normalmente uso const. El let es solo para casos específicos.

 - la función <strong>document.querySelector('')</strong>, selecciona un elemento/documento del site. Por ej.: nav = document.querySelector ('nav');, seleccionará la tag < nav>; produtos = document.querySelector('.produtos a');, seleccionará el "a" que esté dentro de la class='produtos'.
    ¿QUÉ HACEMOS CON EL ELEMENTO SELECCIONADO? después del valor, coloco . y la función que sea. Por ej:
      - produtos.remove(); -> elimina el elemento 'produtos' del DOM;
      - console.log(produtos.href); -> me da el url completo el href de produtos
      - nav.style.backgroundColor = "black";  o  nav.style.padding = "1rem"; -> para modificar un valor de estilo del elemento, como cambiar el bg a negro. 
      - nav.classList.add("ativo"); -> para añadir una clase (en este caso a nav), que se llame .ativo para yo poner estilizarla en el css y que se muestre en el site.