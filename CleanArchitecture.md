### Arquitectura Limpia: Un Camino hacia el Código Sostenible

#### Introducción

En el mundo del desarrollo de software, la **arquitectura juega un papel fundamental**. Una arquitectura bien definida permite crear aplicaciones más fáciles de desarrollar, mantener e implementar. La **Arquitectura Limpia** surge como una metodología para lograr precisamente eso. Este blog explorará en detalle qué es la Arquitectura Limpia, sus conceptos clave y cómo puede beneficiar tus proyectos de software.

#### Objetivos del Blog

*   Definir la Arquitectura Limpia y sus principales características.
*   Explicar los conceptos clave de la arquitectura limpia, como las entidades, casos de uso, adaptadores de interfaz e infraestructura.
*   Presentar los beneficios de la Arquitectura Limpia, incluyendo la facilidad de mantenimiento, la capacidad de prueba y la flexibilidad a los cambios.
*   Proporcionar recursos adicionales para aquellos que deseen profundizar en el tema.

#### Desarrollo

##### Conceptos Clave

La Arquitectura Limpia es una filosofía de diseño de software que se enfoca en la **organización del código en componentes separados y cómo estos se relacionan entre sí**. El objetivo es crear un código con **bajo acoplamiento** y **alta cohesión**, facilitando así su comprensión y mantenimiento. Esta filosofía se basa en la **separación de preocupaciones**, que implica dividir el sistema en módulos con responsabilidades distintas.

Para entender mejor estos conceptos, podemos imaginar una cebolla. En el centro de esta cebolla, encontramos el **Dominio o las reglas de negocio**, que representan la funcionalidad principal de la aplicación. Las capas más externas representan detalles técnicos de implementación, como la interfaz de usuario y la base de datos. Es importante que las capas internas no dependan de las externas, sino al contrario. Esto asegura que los cambios en las capas externas no afecten la lógica de negocio del sistema.

##### Teoría

La Arquitectura Limpia fue propuesta por Robert C. Martin en 2017, en su libro homónimo. Se inspira en ideas como la **Arquitectura Hexagonal** (también conocida como puertos y adaptadores o arquitectura de cebolla) y la **Arquitectura Onion**. Estas arquitecturas enfatizan la importancia de mantener la lógica de dominio en el centro de la aplicación, independientemente de los detalles técnicos externos.

La regla de dependencia de la Arquitectura Limpia indica que las dependencias de código solo pueden ir de las capas externas a las internas. En otras palabras, las capas internas no deben depender de las funciones de las capas externas. Esta regla se basa en el principio de **inversión de dependencias**, el cual establece que las abstracciones no deben depender de los detalles sino que los detalles deben depender de las abstracciones.

Las capas principales de la arquitectura limpia son:

*   **Entidades**: Son las reglas de negocio que son críticas para el funcionamiento de la aplicación, independientes de otras capas.
*   **Casos de uso**: Representan las acciones que un usuario puede realizar en la aplicación y dependen de las entidades.
*   **Adaptadores de interfaz**: Traducen entre el Dominio y la Infraestructura. Aquí se encuentran los modelos, vistas y presentadores.
*   **Infraestructura**: Representa los agentes externos como la interfaz de usuario y la base de datos.
  
![1_gnmlcdpkghf_2f8v3mgtqa.webp](/imagenes/arquitecturaLimpia.svg)

##### Aplicaciones Prácticas

La Arquitectura Limpia es **aplicable a cualquier tipo de proyecto**, desde aplicaciones web hasta aplicaciones móviles. Su enfoque en la separación de preocupaciones y la baja dependencia entre componentes facilita la creación de sistemas escalables y fáciles de mantener. Algunas de las aplicaciones prácticas son:

*   **Desarrollo ágil**: Permite implementar sistemas de software con una sola acción, reduciendo costos y tiempos de trabajo.
*   **Mantenimiento más sencillo**: Facilita la comprensión del código, haciendo más fácil el desarrollo y mantenimiento.
*   **Reducción del riesgo**: Al separar el sistema en componentes, se aísla cada uno a través de interfaces estables, reduciendo el riesgo de errores.
*   **Pruebas más fáciles**: Al tener una arquitectura de complementos, es más fácil probar el código.
*   **Flexibilidad**: Los casos de uso están desacoplados de la interfaz de usuario, permitiendo cambiar la base de datos o el framework web.
*  **Desarrollo en paralelo**: Al estar los componentes aislados, los equipos de desarrollo pueden trabajar en paralelo sin interferir entre ellos

En un ejemplo práctico, una aplicación de comercio electrónico podría tener un dominio que defina la lógica de compra, los casos de uso que incluyan la gestión del carrito de compras, y adaptadores de interfaz para conectarse con una base de datos o una pasarela de pagos. La Arquitectura Limpia también se puede aplicar al desarrollo de microservicios.

**Consideraciones para el MVP**: incluso si estás desarrollando un producto mínimo viable (MVP), es recomendable dedicar tiempo a pensar en la arquitectura del software. Si bien no es necesario implementar todos los aspectos de la Arquitectura Limpia de inmediato, es importante comenzar con una base sólida que permita el crecimiento y la evolución del sistema.

##### Material de Apoyo

*   Ejemplo de implementación en PHP: [https://github.com/hgraca/explicit-architecture-php](https://github.com/hgraca/explicit-architecture-php)
*   Ejemplo de implementación en ReactJS: [https://github.com/hgraca/explicit-architecture-reactjs/tree/workshop-gist_explorer](https://github.com/hgraca/explicit-architecture-reactjs/tree/workshop-gist_explorer)
*   Scaffold para iniciar un proyecto backend con arquitectura limpia: [https://github.com/bancolombia/scaffold-clean-architecture](https://github.com/bancolombia/scaffold-clean-architecture)
*   Guía prescriptiva de AWS sobre arquitecturas hexagonales: [https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/hexagonal-architectures/hexagonal-architectures.pdf](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/hexagonal-architectures/hexagonal-architectures.pdf)
*  Estructura de un proyecto Python en arquitectura hexagonal con AWS Lambda:

#### Conclusión

La Arquitectura Limpia es mucho más que una simple metodología de diseño; es una forma de pensar sobre el desarrollo de software que promueve la **creación de sistemas robustos, flexibles y fáciles de mantener**. Al separar las preocupaciones y establecer límites claros entre los componentes, podemos construir aplicaciones que se adapten mejor a los cambios y evolucionen a lo largo del tiempo. Si bien puede requerir una inversión inicial en la planificación y diseño del sistema, los beneficios a largo plazo hacen que valga la pena adoptarla.

#### Referencias

*   Calderón, N. (2021, 7 de marzo). *Entendiendo a la arquitectura limpia*. Medium. [https://medium.com/@nestorcalderon/entendiendo-a-la-arquitectura-limpia-6d6a2a79d846](https://medium.com/@nestorcalderon/entendiendo-a-la-arquitectura-limpia-6d6a2a79d846)
*   Oruc, F., Goby, D., Kunce, D., & Ploski, M. (2022, junio). *Construyendo arquitecturas hexagonales sobre AWS*. AWS Guía prescriptiva. [https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/hexagonal-architectures/hexagonal-architectures.pdf](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/hexagonal-architectures/hexagonal-architectures.pdf)
*   Graca, H. (2017, 16 de noviembre). *DDD, Hexagonal, Onion, Clean, CQRS, … How I put it all together*. @hgraca. [https://herbertograca.com/2017/11/16/explicit-architecture-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/](https://herbertograca.com/2017/11/16/explicit-architecture-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)


---
### Refererencias
- [Entendiendo a la arquitectura limpia](https://nescalro.medium.com/entendiendo-a-la-arquitectura-limpia-7877ad3a0a47)
- [DDD, Hexagonal, Onion, Clean, CQRS, … How I put it all together](https://herbertograca.com/2017/11/16/explicit-architecture-01-ddd-hexagonal-onion-clean-cqrs-how-i-put-it-all-together/)
- [Construyendo arquitecturas hexagonales sobre AWS](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/hexagonal-architectures/hexagonal-architectures.pdf)

---
### Node
- [Clean Node.js Architecture | Enterprise Node.js + TypeScript](https://khalilstemmler.com/articles/enterprise-typescript-nodejs/clean-nodejs-architecture/)
- [Domain-Driven Hexagon Nodejs](https://github.com/Sairyss/domain-driven-hexagon)
- [Structure your solution by components `#strategic` `#updated`](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-11-structure-your-solution-by-business-components)<
- [Layer your components, keep the web layer within its boundaries `#strategic` `#updated`](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-12-layer-your-components-with-3-tiers-keep-the-web-layer-within-its-boundaries)
- [Wrap common utilities as packages, consider publishing](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-13-wrap-common-utilities-as-packages-consider-publishing)
- [Use environment aware, secure and hierarchical config `#updated`](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-14-use-environment-aware-secure-and-hierarchical-config)
- [Consider all the consequences when choosing the main framework `#new`](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-15-consider-all-the-consequences-when-choosing-the-main-framework)
- [Use TypeScript sparingly and thoughtfully `#new`](https://github.com/goldbergyoni/nodebestpractices/blob/master/README.md#-16-use-typescript-sparingly-and-thoughtfully)
---
### Java
- [Bootcamp: Hablemos de arquitetura hexagonal](https://www.youtube.com/watch?v=m1DnImgmtrM)

