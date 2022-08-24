# template_web_01
Web template without functionality. It's not interactable. 
This is a log for the IH classes in FT_2 and FT_6

¿Qué es VUE?
Un framework de desarrollo web. Básicamente es una herramienta que vamos a utilizar dentro de nuestro Visual Studio Code y que unifica el HTML, CSS y JavaScript. 

¿Dónde me lo descargo?
En este enlace: https://es.vuejs.org/v2/guide/installation.html
Al contrario que las aplicaciones a las que estamos acostumbrado VUE no tiene un instalador, esto es porque no es un programa como tal, que se ejecute. VUE es un conjunto de reglas que se aplican sobre HTML, CSS y JavaScript (JS) así que lo que nos descargamos son los archivos que permiten VIsual Studio Code interpretar dichas reglas. 

(También puedes usar VUE sin descargártelo, añadiendo en el header esto:
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
pero ahora mismo no te lo recomendamos. Si quieres saber más, pincha aquí Getting started quickly (single HTML file))

Como guía resumida usa esta (recuerda usar gitbash y no powershell, y recuerda que tienes que tener node js instalado en tu PC,  que nos conocemos): 
npm install -g @vue/cli 
vue --version ->Compruebas qué versión se te ha instalado y, si no es la que quieres, la fuerzas. 
vue create ‘nombre_de_tu_proyecto’->Aquí instalas la versión de vue concreta que quieras, en nuestro caso vamos a trabajar con la 3. 
npm run serve->Antes de continuar, comprueba que todo está en orden


¿Cómo inicio un proyecto en VUE?
Para guiarnos supongamos que queremos crear una página que se llama WIKI-ROL, una página normal, como tú, que contendrá artículos de una wikipedia. 
Si queremos que WIKI-ROL se programe en VUE lo que debemos hacer es crear un proyecto como lo hemos hecho hasta ahora y a dicho proyecto le instalamos VUE como hicimos en el paso de arriba y voilá nuestro proyecto ya está iniciado. 
Nosotros estamos usando VUE 3, así que descárgate el 3. “Pero es que me he descargado el dos”, pues estás de suerte, porque acabas de empezar el proyecto. Así que bórralo todo y descárgate el 3. 

¿Qué necesito saber para usar VUE?
HTML, CSS y JS. Además de eso, para entender el trabajo con este framework hay que conocer con soltura varios conceptos. 

SPA -> Single Page Application: es una página web que lo hace todo. La idea de VUE es que trabajemos en una única página y que esta no nos redireccione, sino que responda a nuestras necesidades. A esta página que lo gobierna todo podrían haberla llamado Sauron, el Señor del Anillo. Pero en lugar de poner nombres raros decidieron ponerle un nombre intuitivo. Single Page Application hace lo que promete, es como la app de un móvil pero en una única página web. Nuestra spa está por defecto en public/index.html. Lo que significa que ese index es el SPA. 
Componente -> Siguiendo con la manía de llamar a las cosas por su nombre, tenemos los componentes. Que se llaman así porque son los que componen la página. Un componente puede ser una barra de navegación, un footer, un formulario, una imagen dinámica…
Todo componente tiene 3 secciones. <template> (el HTML) | <script> (el JS) | <style> (el CSS)
Elemento estático -> Los elementos estáticos son los que hemos programado hasta ahora, fuera de VUE. Se recomienda programar estos elementos de la manera usual ya que el uso de VUE se reserva a elementos dinámicos. 
Elemento dinámico -> Son elementos que cambian en función a algo. Pueden cambiar con el tiempo, con unos datos que ha introducido el usuario, cada luna llena… lo que tú quieras, pero cambian. 
Archivo JSON -> Son archivos que almacenan datos. Piensa en ellos como si fuesen un documento .txt, son básicos y simples pero muy útiles. Normalmente queremos estos archivos para escribir o recuperar datos que queremos que se mantengan guardados en algún lado. 
DataBase -> Base de datos, es el lugar donde se almacenan todos los datos que la página requiere. Puede ser en formato JSon, excel, txt o usando sistemas intermediarios. Lo que quieras, lo importante es saber que aquí está toda tu info. 
Proxy -> 
Node - NodeJS -> Para lo que nosotros respecta (no se enfaden señores de back-end), es el señor que “lee” el JavaScript en el servidor y lo ejecuta. Sin este señor nuestro código no se ejecutaría. Cuando usamos listeners, este señor es el que está escuchando. 
npm ->
DOM -> Es cómo tienes ordenado el HTML. Cuando hablamos de acceder al DOM o modificar el DOM estamos hablando de insertar código HTML (con su respectivo CSS generalmente) dentro de nuestra página web. 
Import / Export -> 
export default {
 components: {
   ComponentA,
   ComponentB
 },

import NOMBREdelCOMPONENTE from ‘directorio/del/componente.vue’ 

Es la forma que vue tiene de que los componentes se reconozcan entre ellos. Sin estas líneas de código un componente ignorará a otro. 
Import y export se ponen dentro de <script> en un archivo.vue
Prop -> Dependiendo de la rama de programación en la que estés puede significar una cosa u otra. Para nosotros es el diminutivo de “propiedades”. 
Listener -> Son eventos que se lanzan cuando algo sucede. El concepto es que están “escuchando” a ver si algo pasa. 
HTTP y HTTPS -> “Protocolo de tranferencia de hipertexto” y “Protocolo de transferencia de hipertexto segura”. Son los protocolos de comunicación que nos permiten navegar por internet. El segundo tiene un encriptado especial que hace que sea más difícil robar datos. 
Lifecycle methods -> Son los métodos que nos permiten hacer cosas durante un ciclo de vida. El ciclo de vida de un código es crearse - inicializarse - actualizarse - morir. 
En VUE a esto se le llama también crearse - imprimirse en pantalla (montaje) - actualizarse - destruirse o, en inglés, create - mount - update - destroy.
Los Lifecycle methods afectan antes y después de cada una de estas fases pero NUNCA durante la fase. Es decir, puedes llamar al método beforeCreate o created, pero no al método OnCreation como en otros lenguajes de programación. 

¿Y cómo hago para ver mi código de VUE en una web?

Vamos a saltarnos la parte en la que subimos realmente nuestra web a la red porque eso es más complicado. Vamos a centrarnos en crear un servidor personal para poder ver nuestra web, que es algo fácil, sencillo, barato y al alcance de todos. 

Vamos a ejecutar el código directamente desde consola, como hemos visto en clase. Vamos a seguir esta guía, en la sección “running the app locally”

Básicamente es introducir estos comandos: 
npm install vue@latest
npm install --global serve
npm install --global @vue/cli -> Instala las dependencias que ejecutan npm run serve


¿Cómo creo un componente?

Te vas a la carpeta “Components” y creas un archivo acabado en .vue 
Es fácil, sencillo y para toda la familia. 

Añádele tú mismo los componentes <template> <script> y <style>.

¿Cómo exporto un componente?
Imaginemos que estamos haciendo una wikipedia y queremos crear un componente que sea el artículo de la wiki, dicho componente se llama ArticleWiki.vue. 
Dentro del componente, en script, debes poner un cacho de código tal que así: 

export default {
  props: ["msg"],
};

Este código le indica, a quien sea que haga el import, cómo debe leer el componente y qué datos va a recibir del mismo. En este caso el dato que vamos a leer es simplemente un “msg” que será pasado como parámetro. 

Luego te vas al componente donde quieres importar y pones este cacho de código:

<script>
import ArticleWiki from "./components/ArticleWiki.vue";
 
export default {
  components: {
    ArticleWiki: ArticleWiki,
  },
};
</script>

De esta manera el componente que recibe el import recibe los datos del componente exportado. 

Ahora, si queremos llamar al componente en el template deberemos hacer algo tal que así:
<template>
  <div class="main">
    <ArticleWiki msg="holi"></ArticleWiki>
  </div>
</template>

Recuerda que dentro de template debes tener un div que contenga absolutamente todo el código HTML. Template solo puede tener un hijo. El tag se llama como el componente porque lo que hemos creado se puede entender como un “tag personalizado” al que le pasamos determinados valores. 

Copio ambos códigos y cambio los colores. En el siguiente texto dos palabras serán del mismo color cuando estén interrelacionados lógicamente. 

App.vue
<template>
  <div class="main">
    <ArticleWiki msg="holi"></ArticleWiki>
  </div>
</template>
 
<script>
import ArticleWiki from "./components/ArticleWiki.vue";
 
export default {
  components: {
    ArticleWiki: ArticleWiki,
  },
};
</script>


ArticleWiki.vue
<template>
  <div>{{ msg }}</div>
</template>
 
<script>
export default {
  props: ["msg"],
};
</script>

Como ves, en el código que hemos puesto podríamos eliminar la línea de código “props: [“msg”]”. Esa línea actualmente no está haciendo nada. Pero es importante que sepas que ahí van los props. 

¡Enhorabuena! Ya puedes configurar tu primer component. Podrías configurarlo todo en app.vue y, ciertamente, para proyectos pequeños puede que esa sea la opción más rápida, pero no es la mejor. Piensa que una vez crees un component ¡podrás exportarlo a otros proyectos! Esto significa que como programador puedes crear tu propia librería de components y reutilizarla, lo que te permitirá trabajar mejor, más rápido y por ende tener más clientes. 

En resumen: 
Creas el componente dentro de la carpeta components y con formato .vue
Pones el <template> <script> y <style> que quieras para el componente
Dentro de <script> añades el export default y, dentro de dicho export, añades lo que necesites exportar del componente. 
Haces el import donde lo quieras utilizar
Donde lo hayas importado, lo añades a la lista de “components”, que básicamente es la lista de componentes importados para que los puedas utilizar. 


¿Y ahora qué hago con esto?
Ahora viene la parte complicada, crear tu propia web con el diseño y la arquitectura que consideres que va a funcionar. 

Para poder crear tu propia web necesitas conocer las funciones de vue, así que vamos a explicar las funciones básicas de manera abstracta en el siguiente apartado y luego vamos a continuar creando WIKI-ROL, nuestra web normal, como tú. Para crear la web igual damos algún que otro rodeo, pero la idea es simple, enseñarte a hacer una web que contenga todo lo que vamos a ver a nivel teórico. 


¿Cómo importo un css?
Si tienes un style.css que quieres importar íntegramente a tu proyecto de vue lo puedes hacer de forma muy sencilla. 

Crea una copia del archivo
Lleva la copia a src/assets/css
Ve a tu app.vue
En template, dentro de Style escribe @import ‘./src/assets/css---NOMBRE DEL ARCHIVO’
Fin. 

WEB VERSIÓN 0.1
Vamos a crear una web juntos. Para ello vamos a pasar por divesas fases de desarrollo. En la fase 0 vamos a crear una página que no es funcional pero sí estética. Tendrá los componentes visuales que necesitamos. Muchas páginas de negocios pequeños carecen de funcionalidad, son simplemente una página bonita donde dar información a clientes. Posteriormente se les irán añadiendo funcionalidades y, justamente eso, es lo que vamos a hacer nosotros. 

Empezamos la creación de la página web versión 0.1. Te recomiendo que, antes de ponerte a leer abras el proyecto y eches un vistazo a esta versión de la web, para ver qué te encuentras. 

Vamos a crear un Header
Nuestro primer componente va a ser algo sencillo, crearemos un componente llamado Header y, además, jugaremos con fuego. Como sabes existe un tag que se llama header, así, con minúscula, nosotros vamos a crear el tag Header, con mayúscula. Esto no es una buena práctica de programación ya que llamar a dos cosas igual y diferenciarlos simplemente por como se escriben se presta a confusión. Lo vamos a hacer de esta manera solo para mostrarte que se puede hacer y que, si se hace bien, no pasa nada aunque como te digo, hay que intentar evitarlo. 

Para crear nuestro component y luego usarlo ya sabes lo que hacer que hacer. 

En la carpeta components creamos el archivo Header.vue
En el archivo Header.vue ponemos lo que queramos
Importamos el archivo a app.vue
Dentro del <template> de app.vue ponemos un tag que sea <Header>
Fin

Si sigues todos los pasos deberías tener tu flamante Header. Si no, es momento de parar y revisar. Tómate este apartado como un ejercicio ya que simplemente estamos volviendo a hacer lo que ya hemos hecho en apartados anteriores. 

¡Recuerda que el nombre del componente puede darte problemas! Todos los tag son single-word, por ello vue te recomienda (aunque no te obliga) que tus componentes sean multiple-word. Esto significa que tu componente EsteEnCamelCase o que-este-en-kebab.

Si no quieres que vue sea tu amigo y te avise de estas cosas ve a tu vue.config.js y añade esta línea: 
  lintOnSave: false,

Debería quedarte algo tal que así:
const { defineConfig } = require('@vue/cli-service')
module.exports = defineConfig({
  transpileDependencies: true,
  lintOnSave: false,
})
 


Creamos el resto de componentes simples
Entendemos por componente simple aquel que no tiene una lógica compleja detrás. Los componentes que faltan en nuestra web son: 
ArticleWiki: Que contendrá cada uno de los artículos. 
AsideBar: Que contendrá las dos secciones separadas de la wiki, a la izquierda 
FooterBar: Que contendrá una simple línea avisando del copyright
GreatBlock: Que será una imagen central con colorines y un texto

Todos estos elementos tienen una programación simple que vamos a ver a continuación. 

ArticleWiki
Este componente va a cargar el preview de los artículos. 
Para ello, en la línea 6 del código, usamos el v-for para que recorrar el json que tenemos asociado. Le decimos que el key va a ser la id que hay en la base de datos y le asignamos unas clases para luego darle estilo. Fíjate como el key debe ser binding, utilizando los dos puntos. 
Si algo de esto te suena raro, no te preocupes, tú lee los apuntes y cuando llegues a Funciones de vue se hablará de todo esto en más detalle. 
Finalmente cargamos los datos accediendo a las variables. La lógica detrás de esto es la siguiente. 
Cómo leer un json
Para poder leer un json debemos conocer cómo es su estructura interna. En el ejemplo tenemos un json muy simple que nos servirá como primera toma de contacto. El json en cuestión es “Articles.json”. 
Primero debemos cargar el json en el componente, porque si no, el componente no nos va a entender. Por eso en la línea 24 le decimos “oye, componente. Importame una cosa a la que vamos a llamar Articles Wiki y que se encuentra en la carpeta DataBase/Articles.json.”

Cuando el código lo hace, añadimos unas líneas simples en el export. Esas líneas básicamente dicen. 
“Oye, cárgame los datos y en la variable AllArticlesWiki que te estoy declarando, introduce lo que sea que haya en ArticlesWiki”. Ten en cuenta que Data está sirviéndonos para crear variables que tienen dentro un contenido que vamos a necesitar posteriormente. 

Tras ello implementamos ese contenido en el v-for de la línea 6 de código, como hemos dicho antes. Presta especial atención a cuando se usan los dos puntos (:) para bindear algo. Si quitas los dos puntos de la línea 12, tanto en img como en alt, por ejemplo, dejarán de funcionarte las imágenes. 
 
Entendido esto, entiendes todo el componente ArticleWiki.

Aside bar
En este componente vamos a probar a hacer de intermediarios. En lugar de cargar directamente el html en la app.vue vamos a cargarlo en el Aside bar, esto nos permite tener más control sobre qué queremos que se muestre por pantalla y qué no. Además practicamos cómo integrar un componente dentro de otro. 

Si te fijas app.vue nunca llega a cargar ArticleWiki, pero ArticleWiki sí se muestra por pantalla. Esto es porque AsideBar está cargando ArticleWiki y App.vue está imprimiendo por pantalla AsideBar. 
Es como decir “no, yo no tengo dinero, pero tengo una cuenta en el banco que tiene millones de euros”. El concepto es similar, app.vue no tiene a ArticleWiki, pero cuando app.vue quiera puede llamar a AsideBar que le va a dar ArticleWiki. 

En este aside bar aprovechamos para configurar unos inputs que posteriormente nos ayudarán a hacer magia negra buscando cosas. 

Maquetamos
La idea de estos apuntes no es ver css así que he dejado todo el css comentado para que sepas qué hace cada una de las cosas que hay en él. Maqueta la web, eso sí, importando el css adjunto en el github :)

Échale un vistazo también a la parte responsive de la web. 

Fin
Hasta aquí la versión 0.1 de la web. Como puedes observar apenas hemos usado vue para dos o tres cosas pero, conceptualmente, ya nos vamos metiendo en materia. 

¿Qué deberías haber aprendido al hacer esta parte de la web?
Qué es un componente
Cómo se enlazan componentes
Qué es un json
Cómo se recorre un json simple
Cómo se imprime por pantalla información de un json y otros datos
Cómo importar imágenes
Hemos repasado html, css y js

============================================================================================================================================


