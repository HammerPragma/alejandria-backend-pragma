# AWS CLI

## Reto AWS CLI

El reto consiste en usar localstack para simular varios servicios de AWS en nuestra máquina local, lo cual nos obligará a usar únicamente el AWS cli para configurar diferentes servicios, de esta forma al mismo tiempo que aprendemos sobre CLI también aprenderemos algunos de los principales servicios que nos proporciona AWS.

**Objetivo**: El objetivo de este reto es entender el uso del AWS cli para la configuración de funcionalidades AWS, con este curso se espera crear y usar diferentes recursos de AWS únicamente con su cli.

 

**Instalación**:

 

**AWS CLI**: Investigar que es el AWS cli y como es su instalación para diferentes sistemas operativos.

**LocalStack**: Instalar localstack en local para poder simular el uso de servicios AWS.

 

Comandos básicos:

 

aws help: Familiarización con la estructura de comandos y la búsqueda de información específica.

aws configure: Configuración de las credenciales de acceso y la región por defecto.

aws sts get-caller-identity: Verificación de la configuración y la identidad del usuario.

 

Fase 2: Exploración de herramientas básicas:
S3:

	Crear un bucket de s3

	Subir archivo: se debe subir una archivo al bucket anteriormente creado

	Listar buckets creados

 

EC2:

Lanzamiento de instancias: ejecutar una instancia ec2 con cualquier nombre

Conexión a instancias: conectarte a esa instacia

Terminación de instancias: Eliminar instancia

 

RDS:

Crear de una base de datos

Conectarse a la base de datos

Eliminar de la base de datos

 

Fase 3: Profundización en herramientas clave:
 

SQS:

Creación de una cola: Crear una cola SQS en localstack

Envío de mensajes: enviar un mensaje que quede guardado en la cola que creaste

Recepción de mensajes: recibir el mensaje de dicha cola

Eliminación de mensajes: eliminar la cola

 

Lambda:

Creación de una función: crear una función a partir de un código

Invocar la función: invocar la función lambda anteriormente creada

Crear una url de la función

Lamar la url anteriormente creada por medio de curl

 

Dynamo:

	Crear tabla dynamo con la estructura que desees

	Ingresar un elemento a la tabla

	Listar las tablas

---
---

# IAM
[Que es AWS IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

[AWS Manage Policies](https://docs.aws.amazon.com/aws-managed-policy/latest/reference/policy-list.html)

[Tutoriales AWS IAM](https://aws.amazon.com/es/iam/getting-started/)

[Blog AWS IAM](https://aws.amazon.com/es/blogs/mt/)

## Reto IAM

| Paso | Descripción |
|:---:|:---:|
|Entender que es AWS IAM | 1. Entender para que se utiliza AWS IAM. 2. Conceptos básicos: Usuarios, grupos, roles, políticas y permisos. 3. Funciones principales: Administrar usuarios, permisos, roles y políticas.|
|Creación del Usuario | 1. Accede a la consola de administración de AWS y selecciona el servicio IAM. 2. Crea un nuevo usuario con el nombre "UsuarioIAM". |
|Asignación de Permisos | 1. Crea una política con el nombre "PermisoCrearUsuariosIAM". 2. En la sección "JSON", agrega los permisos necesarios. 3. Adjunta la política "PermisoCrearUsuariosIAM" al usuario "UsuarioIAM". |
|Prueba de Acceso | 1. Accede a la consola de administración de AWS con las credenciales del usuario "UsuarioIAM". 2. Selecciona el servicio IAM. 3. Haz clic en "Usuarios" y luego en "Crear usuario". 4. Crea un nuevo usuario con nombre restringido (por ejemplo, "UsuarioCreado"). 5. En la sección "Permisos", selecciona "Adjuntar políticas existentes" y busca la política "IAMFullAccess". Esta política otorga permisos de IAM a los usuarios creados.|

---
---
# SNS 

- [Que es AWS SNS](https://www.youtube.com/watch?v=p1GguDzdYtk)
- [Crea tu primer topico](https://www.youtube.com/watch?v=e9lj0iZ-tgE)
- [Creando topicos SNS](https://www.youtube.com/watch?v=i1su7VVyv-U)
- [AWS SNS Lambda](https://www.youtube.com/watch?v=vwYy8GUV8Zw)
- [Spring + SNS](https://www.youtube.com/watch?v=lF7Ba4-8ER4)
- [NodeJS + SNS](https://www.youtube.com/watch?v=18LSoIt7hKY)

---
---

# AWS SDK
- [AWS SDK](https://keepcoding.io/blog/que-es-aws-sdk/#:~:text=AWS%20SDK%20es%20una%20herramienta,%2C%20JavaScript%2C%20Java%2C%20Ruby%2C)
- [Setup AWS SDK](https://www.youtube.com/watch?v=JufP7cFYwBk)

---
---

# SQS
- [AWS SQS](https://www.youtube.com/watch?v=tafrUi96mj8)
- [Todo lo que deberías saber sobre AWS SQS](https://www.youtube.com/watch?v=Fwnx4jdLxU0)
- [Diferencias entre SNS y SQS](https://www.youtube.com/watch?v=YZG9mW-Rokc)
- [Crea tu primera SQS](https://www.youtube.com/watch?v=sucC6_wSI4U)
- [AWS SQS + LAMBDA](https://www.youtube.com/watch?v=xyHLX1dUwuA)
- [Spring + SQS](https://www.youtube.com/watch?v=q3zo3YREfJI)
- [NodeJS + SQS](https://www.youtube.com/watch?v=_20HXT43hFk)

---
---

# CloudFormation
- [AWS Cloudformation Introduction](https://abiabi0707.medium.com/aws-cloudformation-1a1c90cd1a9f)
- [Tutorial técnico](https://www.youtube.com/watch?v=u4qwcztXhDs)
- [Documentación CloudFormation](https://docs.aws.amazon.com/cloudformation/)

---
---

# KMS y SecretManager

- [Secret Manager](https://abiabi0707.medium.com/aws-secret-manager-f9963a6b4be0)
- [KMS tutorial y casos de uso](https://medium.com/@skpandey8123/demystifying-aws-kms-a-hands-on-guide-with-real-world-scenarios-38f315a4f582)
- [Recuperar y administrar secretos con Lambda](https://medium.com/@gazalofficial30/securesecrets-harnessing-aws-lambda-to-safely-retrieve-and-manage-secrets-in-aws-secrets-manager-3d211eba27bb)
- [Charla AWS KMS](https://www.youtube.com/watch?v=Z8FacXPCkrI)
- [Param Storage y Secret Manager](https://www.youtube.com/watch?v=wlWhk_SGbxM)

---
---

# S3

- [Introducción S3](https://medium.com/edureka/s3-aws-amazon-simple-storage-service-aa71c664b465)
- [Integrar S3 con lambda Functions](https://medium.com/@2017tejasgupta/integrating-amazon-s3-with-lambda-functions-86533b2399cc)

---
---

# DynamoDB

- [Introducción DynamoDB](https://medium.com/@christopheradamson253/deep-dive-into-aws-dynamodb-a-nosql-database-for-high-performance-applications-4c80d1410533)
- [DynamoDB con AWS Lambda](https://manuabhijit.medium.com/aws-lambda-with-dynamodb-269fa5d11a86)

---
---

# StepFunctions

- [Primeros pasos AWS StepFunctions](https://www.youtube.com/watch?v=Zvdf_P5pJis)
- [Tutoriales AWS StepFunctions](https://docs.aws.amazon.com/step-functions/latest/dg/learning-resources.html#tutorials)

---
---

# Lambda
- [Introducción AWS Lambda](https://medium.com/edureka/aws-lambda-tutorial-cadd47fbd39b)
- [AWS Lambda](https://www.youtube.com/watch?v=1wNb_RMvI9E)
- [Charla Lambdas](https://drive.google.com/file/d/1O82nCoUuHqVd6-l4NRK6aObS5FYDrirk/view)


---
---

# Fargate
- [WS Fargate & ECS](https://medium.com/getir/scalable-applications-with-aws-fargate-ecs-32730cc21aec)

---
---

# ECS

- [Introducción ECS](https://medium.com/boltops/gentle-introduction-to-how-aws-ecs-works-with-example-tutorial-cea3d27ce63d)
- [AWS ECS Tutorial](https://www.youtube.com/watch?v=esISkPlnxL0)
- [AWS Tutorial ECS](https://docs.aws.amazon.com/es_es/AmazonECS/latest/developerguide/ecs-tutorials.html)

---
---

# BALANCEADORES

- [Diferencias entre un NBL y ALB](https://medium.com/@eltechno/diferencias-aws-application-load-balancer-alb-vs-network-load-balancer-nlb-235cfde60504)

## Network Load Balancer (NLB)
- [Entendiendo un NLB](https://medium.com/@anirudhadak25/network-load-balancer-4752b17de8f2)
- [Video NLB](https://www.youtube.com/watch?v=ulqYnlwoAiI)
## Application Load Balancer (ALB)
- [ALB Desde 0](https://www.youtube.com/watch?v=FkYaWbI-amo)
- [ALB](https://medium.com/@anirudhadak25/application-load-balancer-113a6fdd62f2)

---
---

# Transitive Gateway

- [Introducción Transitive Gateway](https://medium.com/@christopheradamson253/introduction-to-aws-transit-gateway-simplifying-network-connectivity-9386e31bc20)
- [Mejores practicas Transitive Gateway](https://neal-davis.medium.com/aws-transit-gateway-overview-and-best-practices-a1882d094688)

---
---

# SUBNET

- [Documentación Subnet](https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html)
- [VPC & SUBNETS](https://www.youtube.com/watch?v=TUTqYEZZUdc)
- [Como crear una vpc con una subnet privada y publica](https://www.youtube.com/watch?v=ApGz8tpNLgo)

---
---

# VPC

- [Documentación oficial VPC](https://docs.aws.amazon.com/es_es/vpc/latest/userguide/how-it-works.html)
- [Primeros pasos con VPC](https://medium.com/@rajeshkanumurudevops/basics-of-virtual-private-cloud-42fe927ea857)
- [Tutorial VPC](https://www.youtube.com/watch?v=6a4xu0KadBI)

## Reto VPC

| Paso | Descripción | Recursos |
|:---:|:---:|:---:|
|Crear VPC y subnets | 1. El total de direcciones Ips disponibles para la VPC serán de 16. 2. La VPC debe tener 2 subnets públicas y 2 privadas. | https://aws.amazon.com/es/vpc/ https://aws.amazon.com/es/what-is/cidr/ https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html |
|Crear Instancias EC2 | 1. Debe haber una instancia EC2 publica dentro de la VPC. 2. Debe haber una instancia EC2 privada dentro de la VPC. | |
|Permitir conexión a internet | 1. Debe estar creado y configurado un Internet Gateway para la subnet pública. 2. La tabla de ruta de la subnet pública para que la instancia EC2 pública debe estar configurada para que tenga acceso a internet. 3. Se debe verificar la conexión por medio de SSH a la instancia pública; instala Apache HTTPD para crear un servidor simple y poder acceder por http:80 a un html simple. | https://docs.aws.amazon.com/es_es/efs/latest/ug/wt2-apache-web-server.htmlhttps://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.htmlhttps://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html |
|Configuración Bastion Host y ACL | 1. La instancia EC2 debe funcionar como un Bastion Host para que esta se pueda conectar por SSH a la Instancia privada EC2. Consejo: debes tener un par de claves para poner conectarte a la instancia privada. 3. Las reglas del ACL deben de estar configuradas para prohibir la conexión por HTTP:80 de tu IP a la instancia Ec2 pública. | https://aws.amazon.com/es/solutions/implementations/linux-bastion/ https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html |
|Conexión privada de EC2 con Bucket S3 | 1. El VPC Endpoit debe estar configurado para poder establecer la conexión privada de la instancia EC2 y el Bucket S3 Consejo: Usa la consola para poder verificar la conexión entre los dos servicios. | https://docs.aws.amazon.com/whitepapers/latest/aws-privatelink/what-are-vpc-endpoints.html |
---
---

# X-RAY

- [Introducción XRAY](https://medium.com/@himanshkumar/a-brief-introduction-to-aws-x-ray-1437ac23f549)
- [Explicación XRAY](https://medium.com/@rahulpatelcs/what-is-aws-x-ray-9e5db2cac3c2)
- [Analisis de performace](https://medium.com/@christopheradamson253/aws-x-ray-for-application-performance-analysis-98a82add3cd6)

---
---

# CloudWatch

- [Guia inicial CloudWatch](https://medium.com/@raaj.akshar/a-guide-to-cloudwatch-monitoring-and-alerting-9d44b812a73)
- [Primeros pasos con CloudWatch](https://medium.com/@MetricFire/getting-started-with-aws-cloudwatch-37776c76b5f5)