# picx-gallery description
    Proyecto realizado para FactoríaF5 a modo de prueba técnica, que consiste en la creación de una aplicación  para gestionar las imágenes favoritas de un usuario. 

# IDE (Entorno de desarrollo) y Stack utilizado

- Visual Studio Code
- Vue
- Vuex
- Vuetify
- Sass
- Axios

# Proceso de desarrollo
    Para trabajar en este proyecto empecé abordando el briefing aprovechando las ventajas de mi perfíl. Dado que mi especialidad es el front (que es donde tengo una experiencia real), y es donde creo que puedo hacer un buen trabajo y aportar más al proyecto (respetando los prinicpios SOLID, código limpio y buenas prácticas), es la parte de mi trabajo que me gustaría reflejar y que se valore.

    Opté por hacer una SPA en la que se viera el listado de imágenes, ya que creo que bien estructurada daría al usuario una buena experiencia a la hora de utilizarla.

    Sirviéndome de axios, utilicé una API (la pokeapi, ya que es la que más facilidad de uso e información me permitía) para hacer un mock de la información de la página.

    Una vez conseguida la información para el proyecto, planteé una estructura básica, para que todas las imágenes se muestren de la misma manera. Utilicé un grid responsive para que la galería se adapte a diferentes dispositivos y permita una mejor usabilidad.

    Las imágenes se muestran en tarjetas, que tienen como elemento principal la propia imagen, y van acompañadas de un título (en este caso el nombre del pokemon) y una descripción, que permitirá al usuario una mejor contextualización de la imagen al poder aportar información más completa de esta.

    Decidí hacer el proyecto en VUE, ya que es un framework que conozco y con el que actualmente trabajo y me desenvuelvo bien. Además, para sacarle más partido a VUE (y viendo el tiempo con el que contaba para hacer el proyecto), integré vuetify, que me facilita la creación de componentes y estructuración del proyecto, y me permite construir estructuras de manera rápida. También para mejorar la eficiencia de mi código trabajé con sass, aprovechando la modularización de los estilos y el potencial que puede llegar a tener el proyecto con este preprocesador.

    La toma de decisiones para el stack del proyecto está basada en el presente y en el futuro del mismo. Me gustaría seguir trabajando en PicxGallery para crear diferentes vistas y mejorar las funcionalidades del proyecto, así como añadir nuevos componentes que aporten valor y permitan una mejor interacción al usuario(por ejemplo una sección de imágenes destacadas, incluir diferentes galerías, permitir dos tipos de visualización del contenido, la sección de favoritos...), y se que con la estructura que he planteado me resultaría sencillo hacer un proyecto tan escalable.

## Project setup
```
npm install
```
Remember to switch to the right folder on console -> cd picx-gallery

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
