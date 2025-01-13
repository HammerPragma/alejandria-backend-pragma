
**Título: Gestionando la Configuración de forma Segura y Eficiente con AWS Systems Manager Parameter Store**

**Introducción**

En el mundo de la computación en la nube, **la gestión de la configuración** es un componente vital para construir y mantener sistemas robustos y escalables. **AWS Systems Manager Parameter Store** (SSM Parameter Store) es un servicio que proporciona un almacenamiento centralizado y seguro para gestionar datos de configuración y secretos. Este blog explorará en profundidad qué son los parámetros de SSM, sus casos de uso comunes dentro de AWS CDK, y cómo sacar el máximo provecho de esta funcionalidad. El objetivo es proporcionar una guía clara y práctica para desarrolladores y profesionales de TI que buscan optimizar la gestión de la configuración en AWS.

![ssm](/imagenes/ssm.webp)

**Desarrollo**

*   **Conceptos Clave:**
    *   **¿Qué son los Parámetros SSM?** SSM Parameter Store es un servicio dentro de AWS Systems Manager que permite almacenar datos de configuración de forma jerárquica y segura. Estos parámetros pueden contener información variada, desde datos en texto plano como cadenas de conexión a bases de datos, hasta información sensible como contraseñas.

    *   **Características Principales:**
        *   **Almacenamiento Seguro:** Ofrece cifrado para datos sensibles.
        *   **Organización Jerárquica:** Permite agrupar parámetros lógicamente.
        *   **Control de Versiones:** Mantiene un historial de cambios en los parámetros.
        *   **Integración:** Funciona con otros servicios y aplicaciones de AWS.
        *   **Control de Acceso:** Utiliza IAM para una gestión de acceso detallada.
        *   **Centralización:** Proporciona una ubicación centralizada para la configuración.

*   **Teoría:**
    *   **Infraestructura como Código (IaC):** La gestión de la configuración ha evolucionado con la adopción de IaC, donde la infraestructura se gestiona mediante archivos de datos de configuración. AWS CDK utiliza `aws-ssm` para crear y referenciar parámetros SSM.
    *  **Integración con AWS CDK**:
        *   **Creación:** En CDK, los parámetros se crean utilizando `ssm.StringParameter()`.
        *   **Referencias Dinámicas:** CDK genera plantillas de CloudFormation que referencian los parámetros en tiempo de despliegue. Se utilizan formatos como `{{resolve:ssm:reference-key:version}}` para parámetros de texto plano y `{{resolve:ssm-secure:reference-key:version}}` para cadenas seguras.
        *  **Parámetros de Plantilla:** Se pueden crear parámetros de CloudFormation que toman valores de los parámetros de SSM, aunque estos pueden quedar expuestos en la consola de CloudFormation.
    *   **Métodos de Lookup**: CDK puede buscar parámetros SSM usando `valueFromLookup()`, que invoca el SDK de AWS y almacena los valores en el archivo `cdk.context.json`.

*   **Aplicaciones Prácticas:**
    *   **Referenciar AMIs:** Almacenar el ID de una AMI en un parámetro SSM y referenciarlo al crear una instancia EC2.
    *   **Configurar Grupos de Seguridad:** Utilizar un parámetro SSM para la descripción de un grupo de seguridad.
    *   **Manejo de Secretos:** En lugar de pasar valores directamente a recursos como Lambda, se pasa el nombre del parámetro y se permite que el recurso lo resuelva. Si el servicio no soporta ssm-secure, se recomienda usar `secretsmanager` para almacenar la información sensible.
    *   **Uso con Lambda:** Utilizar extensiones de Lambda para recuperar valores de parámetros en lugar de exponerlos como variables de entorno.
    *  **Compartir Parámetros entre Cuentas:** Se utiliza `fromStringParameterArn()` para referenciar un parámetro en otra cuenta, siempre que esté en la capa avanzada, compartida vía AWS RAM y la cuenta consumidora acepte la invitación.
    *  **Despliegue Multi-Región:** Para referenciar parámetros SSM en otras regiones, es necesario utilizar recursos personalizados o crear copias de los parámetros en la región actual.

*  **Material de Apoyo:**
    *   **Documentación de AWS:**
        *   Introducción a AWS Secrets Manager: [https://aws.amazon.com/secrets-manager/](https://aws.amazon.com/secrets-manager/)
        *   Documentación de AWS Secrets Manager: [https://docs.aws.amazon.com/secretsmanager/](https://docs.aws.amazon.com/secretsmanager/)
        *   Documentación de AWS Systems Manager Parameter Store: No se proporciona el link exacto, pero se infiere que es parte de la documentación principal de AWS Systems Manager.
    *  **Tutoriales y Artículos:**
        *   Tutorial para almacenar secretos con AWS Secrets Manager: [https://www.geeksforgeeks.org/what-is-aws-secrets-manager/](https://www.geeksforgeeks.org/what-is-aws-secrets-manager/)
        *   Integración de AWS Secrets Manager con Java: Varias fuentes sobre la integración con Java, Spring Boot y AWS Lambda.
        *  Mejores prácticas para usar AWS Secrets Manager: [https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/secure-sensitive-data-secrets-manager-terraform/best-practices.html](https://docs.aws.amazon.com/es_es/prescriptive-guidance/latest/secure-sensitive-data-secrets-manager-terraform/best-practices.html)
    *   **Videos:**
        *   Mejores prácticas en gestión de secretos con AWS Secrets Manager: [https://www.youtube.com/watch?v=HxdypPHilow](https://www.youtube.com/watch?v=HxdypPHilow)
        *  Spring Boot 3.0 integration with AWS Secrets Manager: [https://www.youtube.com/watch?v=1j028KYS4ps](https://www.youtube.com/watch?v=1j028KYS4ps)
   *  **Consideraciones Adicionales:**
        *  Al usar `valueFromLookup()`, hay que ser conscientes de que el valor se expone en la plantilla de CloudFormation y se guarda en el archivo `cdk.context.json`. Es importante gestionar el caché y utilizar `cdk context --reset` cuando sea necesario.
        * Al usar  referencias dinámicas, el valor podría quedar expuesto en la consola del recurso destino.
        *  Es vital proteger la información sensible almacenando como `SecureString` y usar `secretsmanager` cuando sea necesario.

**Conclusión**

**AWS Systems Manager Parameter Store** es una herramienta esencial para la gestión de la configuración en AWS, facilitando la centralización, seguridad y control de la información de configuración. Integrado con AWS CDK, permite una gestión de infraestructura como código más eficiente. Es vital comprender las diferentes formas de referenciar los parámetros (referencias dinámicas, parámetros de plantilla, lookup) y las consideraciones de seguridad que conllevan. Al seguir las mejores prácticas y utilizar las herramientas adecuadas, se pueden construir sistemas más robustos y seguros.
