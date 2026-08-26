# Documentacion_ProyectoAPT_Code-Trekking
ProyectoAPT_Code-Trekking

**Elemento requerido en readme** 

### **Nombre del proyecto:** 
Code-Trekking - Aplicación móvil de trekking colaborativo y seguro.

### **Descripción:** qué hace, a quién va dirigido, qué problema resuelve

*Que hace:* 
  
  Code-Trekking es una aplicación móvil desarrollada para personas interesadas en realizar actividades de trekking en la Región Metropolitana de Chile.
  
  El proyecto busca facilitar la organización de actividades grupales de trekking mediante una plataforma que permita a los usuarios encontrar compañeros, crear y participar en eventos, consultar información sobre rutas   y comunicarse con otros participantes.
  
  Además, la aplicación incorpora funcionalidades orientadas a la seguridad, como seguimiento de ubicación mediante GPS, registro del recorrido y un botón SOS que permite compartir la ubicación del usuario con sus         contactos de emergencia.

*A quién va dirigido:* 

  La aplicación está dirigida principalmente a:
  
  - Personas adultas interesadas en realizar trekking.
  - Personas que están comenzando a practicar trekking.
  - Personas con experiencia que buscan nuevas rutas.
  - Personas que no cuentan con un grupo para realizar actividades.
  - Organizadores de actividades de trekking.
  
  Inicialmente, el proyecto se encuentra orientado a usuarios de la Región Metropolitana de Chile.

*Qué problema resuelve:*

  Las personas interesadas en realizar trekking pueden presentar dificultades para:
  - Encontrar personas que compartan el mismo interés y disponibilidad.
  - Organizar actividades grupales de manera sencilla.
  - Acceder a información centralizada sobre las rutas.
  - Conocer características técnicas de una ruta antes de realizarla.
  - Mantener comunicación con los participantes de una actividad.
  - Contar con herramientas de ubicación y comunicación ante una emergencia.
  
  Actualmente, estas necesidades suelen resolverse utilizando diferentes plataformas y aplicaciones de manera independiente.
  
  Code-Trekking busca centralizar estas funcionalidades en una sola aplicación móvil, proporcionando una experiencia colaborativa y orientada a la seguridad.

### **Tecnologías utilizadas (lenguajes, frameworks, base de datos, cloud):**

- Angular — Framework principal para el desarrollo de la aplicación.
- Ionic Framework — Componentes de interfaz y desarrollo de la aplicación móvil.
- TypeScript — Lenguaje principal del proyecto.
- HTML5 — Estructura de las interfaces.
- SCSS / CSS — Estilos y diseño visual.
- Firebase Authentication — Autenticación y gestión de usuarios.
- Cloud Firestore — Base de datos NoSQL en la nube.
- Firebase Security Rules — Control de acceso y seguridad de los datos.

### **Instrucciones para ejecutar el proyecto localmente:** 

Antes de ejecutar el proyecto es necesario contar con:

- Node.js instalado.
- npm instalado.
- Angular CLI.
- Ionic CLI.
- GitHub.
- Actions de Github, si se desea ejecutar la aplicación como aplicación Android (APK).
- Una cuenta/proyecto de Firebase configurado.
- Las credenciales correspondientes a los servicios externos utilizados por la aplicación.

Se recomienda utilizar una versión de Node.js compatible con la versión de Angular utilizada por el proyecto.

1. Clonar el repositorio
- git clone https://github.com/DaniloGCh/code-trekking.git

Ingresar al directorio del proyecto:

- cd Trekking-Link

2. Instalar las dependencias

Ejecutar:

- npm install

3. Configurar las variables de entorno (modifcar esta parte)

Antes de ejecutar la aplicación se deben configurar las credenciales necesarias para los servicios externos.

4. Ejecutar la aplicación en el navegador

Para iniciar el servidor de desarrollo:

- ionic serve

También puede utilizarse:

- ng serve

Luego acceder desde el navegador a:

- http://localhost:8100

Generar APK para Android:

- La aplicación Android se genera automáticamente mediante **GitHub Actions**, por lo que no es necesario abrir el proyecto en Android Studio para generar la APK.


### **Integrantes del equipo con sus roles** 

- Ismael Horta - Rol: (agregar roles)
- Danilo González - Rol: (agregar roles)

Ambos integrantes participan en las actividades de análisis, diseño, desarrollo, pruebas, documentación y toma de decisiones del proyecto.

### **Metodología de trabajo del equipo (Scrum, Kanban, DevOps, etc.)** 

El desarrollo de Code-Trekking utiliza la metodología ágil Scrum.

El proyecto se organiza en 18 sprints semanales, permitiendo dividir el desarrollo en incrementos funcionales y realizar revisiones periódicas del avance.

Fases del proyecto:

Fase 1 — Definición (S1-S4):
Fase 2 — Desarrollo (S5-S15):
Fase 3 — Cierre (S16-S18)

### **Arquitectura de la solución (descripción o diagrama)** 

Code-Trekking utiliza una arquitectura modular separando la presentación, lógica de negocio, acceso a datos y servicios externos.

La aplicación está desarrollada utilizando Angular como framework principal, Ionic para la interfaz móvil, Firebase para autenticación y persistencia de datos y Capacitor para acceder a funcionalidades nativas del dispositivo.

┌──────────────────────────────────────────────┐ │ CODE-TREKKING │ │ Aplicación móvil │ └──────────────────────┬───────────────────────┘ │ ▼ ┌──────────────────────────────────────────────┐ │ CAPA DE PRESENTACIÓN │ │ │ │ Angular + Ionic │ │ │ │ Login | Register | Home | Perfil │ │ Eventos | Foro | Mapa | Dashboard │ └──────────────────────┬───────────────────────┘ │ ▼ ┌──────────────────────────────────────────────┐ │ LÓGICA DE NEGOCIO │ │ │ │ Services │ │ ├── auth.service.ts │ │ ├── evento.service.ts │ │ ├── security.service.ts │ │ ├── tracking.service.ts │ │ ├── foto.service.ts │ │ ├── sos.service.ts │ │ ├── session.service.ts │ │ ├── lugar.service.ts │ │ ├── consejo.service.ts │ │ └── weather-global.service.ts │ │ │ │ Guards + Interceptors │ └──────────────────────┬───────────────────────┘ │ ▼ ┌──────────────────────────────────────────────┐ │ CAPA DE DATOS │ │ │ │ TypeScript Models │ │ │ │ Firebase Authentication │ │ Cloud Firestore │ │ Local Storage │ └──────────────────────┬───────────────────────┘ │ ▼ ┌──────────────────────────────────────────────┐ │ SERVICIOS EXTERNOS / CLOUD │ │ │ │ Firebase │ │ OpenRouteService │ │ OpenWeatherMap │ │ OpenStreetMap │ │ OpenTopoMap │ │ Esri │ │ Thunderforest │ │ Wikiloc │ └──────────────────────┬───────────────────────┘ │ ▼ ┌──────────────────────────────────────────────┐ │ CAPACITOR / HARDWARE │ │ │ │ GPS │ │ Cámara │ │ Compartir │ │ Portapapeles │ │ Background Geolocation │ └──────────────────────────────────────────────┘


