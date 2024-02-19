# 1. Instalar Ruby
Ruby [instalador](https://rubyinstaller.org/downloads/)

# 2. Instalación de Jekyll
```
gem install jekyll bundler
```
## 3. Crear un Nuevo Sitio Jekyll
```
jekyll new mi-sitio-web
```
## 4. Cambios para que funcione correctamente
A la hora de hacer el proyecto en el archivo **Gemfile** hay que añadir cambiar el código por el siguiente:

```
# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll", "~> 4.3.3"

gemspec
gem 'jekyll-remote-theme'

```
Sino no te permitirá modificar el css posteriormente.

## 5. Servir tu Sitio Localmente
```
cd mi-sitio-web
```
```
bundle exec jekyll serve
```

# 6. Modificación de css

Ir a **nombre_de_TÚ_proyecto** > assets > css > style.css. 

por ejemplo:
```
---
---

@import 'jekyll-theme-leap-day';

header{
    background: black;


    h1{
        color: aliceblue    ;

    }
}

body{
    background: white;
    
}

#banner {
    background-color: aquamarine;
}
```



# 7. Header

A la hora de crear el **header** he tenido los siguientes **problemas**:

- La barra de navegación de la Izquierda la genera en base a los **nav**. 

    Si pones el siguiente código, se ve de la siguiente manera:
    ```
         
        <!--
        <nav id="indice">-->
                
            <ul>
                <li><a href="#"></a></li>
            </ul>
        <!--</nav> -->

    ```


<center>

![Sin](./docum-XPOL/fotos_doc/header_con_nav.png)

![Con](./docum-XPOL/fotos_doc/header_con_nav.png)
</center>

Hay que redirecciónar de la siguiente manera:

```
    <li><a href="../docs/nombre_del_documento_markdown.html">nombre de la página</a></li>
```

JEKYLL VS MDOCS

MKDOCS
Ventajas:

Enfoque en la documentación: MkDocs está específicamente diseñado para la documentación de proyectos, lo que significa que muchas de sus características y su estructura están optimizadas para este fin.
Facilidad de uso: Tiene una curva de aprendizaje baja, especialmente si ya estás familiarizado con Markdown. Configurar un sitio de documentación es rápido y sencillo.
Personalización: El tema Material para MkDocs ofrece un diseño moderno y es altamente personalizable, permitiendo ajustes a través de la configuración sin necesidad de tocar mucho el código.
Búsqueda integrada: Incluye un potente sistema de búsqueda que facilita a los usuarios encontrar la información que necesitan dentro de tu documentación.
Comunidad activa: Hay una comunidad activa alrededor de MkDocs y el tema Material, lo que significa que hay muchos recursos, plugins y soporte disponible.
Desventajas:

Menos flexibilidad para sitios no documentales: Aunque es altamente personalizable dentro de su ámbito, puede ser menos flexible que Jekyll para crear sitios web que no sean estrictamente de documentación.
Menos temas y plugins en comparación con Jekyll: Aunque hay una buena cantidad disponible, puede ser limitante si buscas una funcionalidad muy específica que no está cubierta.
Tiempo de aprendizaje: Generalmente bajo. Podrías empezar a producir documentación en unas pocas horas hasta un par de días, dependiendo de la complejidad de tus necesidades de personalización.

Jekyll
Ventajas:

Flexibilidad: Jekyll es extremadamente flexible y puede ser utilizado para construir casi cualquier tipo de sitio web estático, no solo documentación.
Gran ecosistema: Hay una enorme cantidad de temas y plugins disponibles, lo que te permite extender la funcionalidad de tu sitio de maneras complejas.
Integración con GitHub Pages: Jekyll es compatible de forma nativa con GitHub Pages, lo que facilita la publicación de tu documentación sin necesidad de servidores adicionales.
Comunidad grande: Al ser uno de los generadores de sitios estáticos más antiguos y populares, cuenta con una amplia comunidad y muchos recursos disponibles.
Desventajas:

Curva de aprendizaje más elevada: Debido a su flexibilidad y amplia gama de funciones, puede llevar más tiempo aprender a usar Jekyll eficazmente, especialmente si quieres personalizar tu sitio a fondo.
Velocidad de construcción: Para proyectos grandes, Jekyll puede ser más lento en la generación del sitio comparado con MkDocs.
Tiempo de aprendizaje: Moderado a alto. Puedes necesitar desde unos días hasta unas semanas para sentirte cómodo con todas las herramientas y opciones de personalización que ofrece Jekyll.

Conclusión
La elección entre MkDocs con Material y Jekyll depende en gran medida de tus necesidades específicas de documentación y tu familiaridad previa con tecnologías web. Si buscas una solución específicamente optimizada para documentación que sea fácil de usar y configurar, MkDocs con Material puede ser la mejor opción. Por otro lado, si necesitas más flexibilidad para crear un sitio web más complejo o integrado y no te importa una curva de aprendizaje más pronunciada, Jekyll podría ser más adecuado.





