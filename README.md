Este proyecto es una aplicación sencilla en Vue.js que permite obtener datos de diferentes APIs, mostrando manga, anime, población de países y recomendaciones de anime.

## Descripción

La aplicación cuenta con cuatro botones que permiten al usuario obtener diferentes tipos de datos aleatorios o de consulta a través de llamadas a APIs externas:

- **Random Manga**: Obtiene un manga aleatorio desde la API de Jikan.
- **Random Anime**: Obtiene un anime aleatorio desde la API de Jikan.
- **Random Country**: Obtiene datos de la población de países usando la API de Countries Now.
- **Random Anime Recommendations**: Obtiene recomendaciones de anime desde la API de Jikan.

Cada consulta realizada a las APIs muestra los resultados en pantalla bajo el botón correspondiente.

## Estructura del Proyecto

El proyecto cuenta con los siguientes componentes principales:

- **App.vue**: Componente raíz de la aplicación que contiene el layout básico.
- **APIData.vue**: Componente que gestiona las llamadas a las APIs y la visualización de los datos obtenidos.
