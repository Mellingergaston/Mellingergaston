<div align="center">

# Hola, soy Gastón Mellinger 👋

### Estudiante de Ingeniería en Sistemas · Full Stack Developer · Co-founder de [Zonea](https://zonea.app)

Construyo productos de software de punta a punta: desde el análisis del problema y el diseño de la arquitectura hasta la implementación, testing y deploy.

[![Zonea](https://img.shields.io/badge/Zonea-zonea.app-10172a?style=for-the-badge&logo=googlechrome&logoColor=white)](https://zonea.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Gastón%20Mellinger-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gaston-mellinger-14997542a/)
[![Email](https://img.shields.io/badge/Email-Contacto-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:gaston.mellinger1@gmail.com)

<br>

![UNS](https://img.shields.io/badge/UNS-Ingeniería%20en%20Sistemas-1e3a8a?style=flat-square)
![Argentina](https://img.shields.io/badge/Bahía%20Blanca-Argentina-74acdf?style=flat-square)

</div>

---

## 👋 Sobre mí

Soy estudiante avanzado de **Ingeniería en Sistemas de Información en la Universidad Nacional del Sur** y desarrollador web full stack.

Me interesa construir sistemas completos: entender el dominio, transformar requerimientos en decisiones de diseño y llevar esas decisiones hasta producción.

Actualmente soy cofundador y desarrollador de **[Zonea](https://zonea.app)**, una plataforma para la gestión de torneos de pádel que se comercializa a clubes.

A lo largo de la carrera y de mis proyectos trabajé con desarrollo web, arquitectura de software, bases de datos, testing, programación lógica, algoritmos, programación concurrente y sistemas operativos.

> Me interesa entender cómo funcionan los sistemas, diseñarlos correctamente y después llevarlos a código.

---

# ⭐ Proyecto principal

## 🎾 [Zonea](https://zonea.app) — Gestión de torneos de pádel

[![Producción](https://img.shields.io/badge/Estado-En%20producción-16a34a?style=flat-square)](https://zonea.app)
[![Web](https://img.shields.io/badge/Web-zonea.app-10172a?style=flat-square&logo=googlechrome&logoColor=white)](https://zonea.app)

**Zonea** es una plataforma web que desarrollamos desde cero junto a [Lucas Bertone](https://github.com/Lucasbertone02) para automatizar la organización de torneos de pádel.

El sistema reemplaza gran parte del trabajo manual del organizador: genera zonas respetando rankings, arma llaves, asigna horarios considerando disponibilidad de jugadores y canchas, actualiza rankings y publica toda la información del torneo para los jugadores.

### Funcionalidades

- 🏆 **Múltiples formatos de torneo:** clásico, americano por parejas, americano individual y ligas.
- 🧩 **Generación automática de zonas y llaves**, incluyendo cabezas de serie, byes y criterios deportivos.
- 🗓️ **Motor propio de asignación de horarios** considerando disponibilidad, canchas, descansos y torneos simultáneos.
- ↕️ **Editor visual drag & drop** para modificar la programación.
- 📊 **Rankings por club y categoría**, con historial de puntos y ascensos.
- 🔗 **Torneos públicos sin login** para consultar zonas, partidos, resultados y llaves.
- 🖼️ **Generación de imágenes para redes sociales** con la identidad visual de cada club.
- 📄 **Planillas PDF** para imprimir durante el torneo.
- 📺 **Modo TV** para mostrar partidos, resultados, avisos y sponsors dentro del club.
- 💳 **Administración de clubes, planes y facturación.**

<details>
<summary><strong>🏗️ Ingeniería detrás de Zonea</strong></summary>

<br>

### Arquitectura

El sistema utiliza un **monolito modular organizado por capas**, manteniendo el dominio desacoplado del framework mediante conceptos inspirados en arquitectura hexagonal.

Las dependencias permitidas entre capas se validan automáticamente utilizando ESLint.

Algunos de los patrones y conceptos utilizados:

`Repository` · `Adapter` · `Dependency Injection` · `Observer` · `Strategy` · `Factory` · `Value Objects`

### Multi-tenancy

La plataforma utiliza PostgreSQL compartido entre clubes.

El aislamiento de información se implementa mediante **Row Level Security**, mientras que las operaciones sensibles utilizan transacciones y bloqueos para mantener consistencia frente a operaciones concurrentes.

### Algoritmos

Zonea incluye algoritmos propios para resolver distintos problemas del dominio:

- asignación de horarios basada en restricciones;
- búsqueda y reparación de conflictos;
- generación de llaves con byes;
- distribución de cabezas de serie;
- generación de fixtures mediante el método del círculo.

### Testing

El proyecto cuenta con **más de 200 archivos de tests con Vitest**, incluyendo:

- tests unitarios;
- tests de casos de uso;
- contratos de repositorios;
- integración con PostgreSQL.

### Proceso de desarrollo

Trabajamos siguiendo un proceso incremental:

`Relevamiento` → `Especificación` → `Diseño` → `ADRs` → `Implementación` → `Testing` → `QA` → `Deploy`

Las decisiones arquitectónicas importantes quedan documentadas mediante **Architecture Decision Records**.

</details>

### Stack

`Next.js` · `React` · `TypeScript` · `Tailwind CSS` · `shadcn/ui` · `Prisma` · `PostgreSQL` · `Supabase` · `Auth.js` · `Zod` · `Satori` · `pdf-lib` · `Upstash` · `Resend` · `Vitest` · `Vercel`

---

# 📂 Otros proyectos

## 🚗 AlquilAutos

**Ecosistema de alquiler de autos**

`Ingeniería de Aplicaciones Web` · `Equipo de 6` · `2026`

Marketplace compuesto por varias aplicaciones independientes que se comunican mediante **APIs REST** para manejar compradores, propietarios, pagos, entregas, reseñas y métricas.

### Mi aporte

Fui desarrollador principal de la **Seller App**, encargada de la operación del propietario.

- Gestión completa de vehículos.
- Carga de imágenes mediante Cloudinary.
- Ciclo de vida de reservas con **8 estados**.
- Operaciones críticas protegidas mediante transacciones.
- Panel de ingresos y administración.
- API REST utilizada por las demás aplicaciones.
- Autorización mediante roles.

También participé en el desarrollo de un **Analytics Dashboard** que consulta en paralelo las distintas aplicaciones del ecosistema y consolida sus datos en KPIs, gráficos, rankings y alertas.

**Conceptos aplicados**

`REST APIs` · `Repository` · `Service Layer` · `Server Actions` · `Transacciones` · `RBAC` · `Analytics`

**Stack**

`Next.js` · `React` · `TypeScript` · `Tailwind CSS` · `Prisma` · `PostgreSQL` · `Neon` · `Clerk` · `Zod` · `Cloudinary` · `Recharts` · `ExcelJS` · `jsPDF`

[![Seller App](https://img.shields.io/badge/Demo-Seller%20App-000000?style=flat-square&logo=vercel&logoColor=white)](https://proyecto-c-seller-alquilautos.vercel.app/)
[![Repo Seller](https://img.shields.io/badge/Repo-Seller%20App-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IAW-2026/proyecto-c-seller-alquilautos)
[![Analytics](https://img.shields.io/badge/Demo-Analytics-000000?style=flat-square&logo=vercel&logoColor=white)](https://etapa-3-analytics-dashboard-alquila.vercel.app/)
[![Repo Analytics](https://img.shields.io/badge/Repo-Analytics-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IAW-2026/etapa-3-analytics-dashboard-alquilautos)

---

## 🗓️ SalePadel

**Turnero y gestión para complejos de pádel**

`Arquitectura y Diseño de Software` · `Trabajo en equipo` · `2026`

Aplicación web donde los jugadores pueden reservar canchas, crear lobbies para completar partidos y evaluarse después de jugar.

Desde el lado del complejo se pueden administrar canchas, bloqueos, reservas y reportes.

### Ingeniería del proyecto

El desarrollo recorrió gran parte del ciclo de diseño de software:

- requerimientos funcionales y no funcionales;
- casos de uso;
- reglas de negocio;
- estudio de viabilidad;
- diagramas **C4**;
- modelo de datos;
- documentación mediante **ADRs**;
- especificación de APIs.

La implementación sigue una arquitectura:

`Routes` → `Services` → `Repositories`

También utilizamos **Observer** para desacoplar las notificaciones mediante eventos.

El sistema incluye además:

- finalización automática de turnos mediante GitHub Actions;
- reportes en Excel y PDF;
- notificaciones por correo;
- pronóstico del clima utilizando OpenWeather;
- mapas utilizando Leaflet.

**Stack**

`Next.js` · `React` · `TypeScript` · `Tailwind CSS` · `Radix UI` · `Prisma` · `PostgreSQL` · `Clerk` · `Nodemailer` · `Recharts` · `GitHub Actions` · `Vercel`

[![Demo](https://img.shields.io/badge/Demo-SalePadel-000000?style=flat-square&logo=vercel&logoColor=white)](https://proyecto-turnero-ay-d.vercel.app/)
[![Repo](https://img.shields.io/badge/Repo-SalePadel-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/LautyNahid/proyecto-turnero-AyD)

---

## 🍄 Super Mario 2D

**Videojuego de plataformas desarrollado desde cero en Java**

`Tecnología de Programación` · `Equipo de 5` · `2025`

Proyecto desarrollado en equipo donde primero diseñamos la estructura del sistema, las responsabilidades de las clases y los patrones a utilizar antes de comenzar con la implementación.

El juego cuenta con:

- tres niveles cargados desde archivos de texto;
- seis tipos de enemigos;
- power-ups;
- dos skins;
- sistema de puntaje;
- ranking;
- sonido;
- scrolling horizontal.

### Lo interesante técnicamente

- Game loop propio.
- Detección de colisiones mediante hitboxes.
- Jerarquía de entidades.
- Separación de responsabilidades mediante patrones de diseño.

**Patrones utilizados**

`State` · `Abstract Factory` · `Visitor` · `Template Method`

**Stack**

`Java 17` · `Swing` · `AWT` · `Eclipse`

[![Repo](https://img.shields.io/badge/Repo-SuperMario2D-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Mellingergaston/SuperMario2D)

---

## 🧩 M2 Blocks

**Puzzle web con motor lógico desarrollado en Prolog**

`Lógica para Ciencias de la Computación` · `Trabajo en equipo` · `2025`

Juego donde bloques numerados se disparan sobre una grilla y deben combinarse siguiendo distintas reglas.

Una de las características principales del proyecto es que **la lógica del juego está implementada en Prolog**, mientras que la interfaz está desarrollada en React.

La comunicación entre ambos sistemas se realiza mediante **SWI-Prolog Pengines**.

### Mi aporte

Mi trabajo se concentró principalmente en el motor de reglas en Prolog y en la coordinación del flujo de juego desde React.

El motor implementa:

- combinaciones horizontales;
- combinaciones verticales;
- combinaciones triples;
- estructuras en L y T;
- resolución de combinaciones en cascada;
- gravedad invertida por columna;
- progresión y desbloqueo de bloques;
- generación del siguiente bloque;
- sistema de hints.

**Conceptos aplicados**

`Logic Programming` · `Rule Engine` · `Recursión` · `Backtracking` · `Pengines`

**Stack**

`Prolog` · `SWI-Prolog Pengines` · `React` · `TypeScript` · `CSS`

[![Repo](https://img.shields.io/badge/Repo-M2%20Blocks-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/LCC-DCIC-UNS-2025/proyecto-m2blocks-com-20)

---

# ⚙️ Programación de sistemas

Además del desarrollo web, tengo formación práctica en **programación de sistemas, concurrencia y sistemas operativos utilizando C sobre Linux**.

### Procesos e IPC

- Desarrollo de programas concurrentes en **C**.
- Creación y gestión de procesos mediante `fork`, `exec` y `waitpid`.
- Comunicación entre procesos utilizando **pipes**.
- Trabajo con **colas de mensajes**.
- Uso de **memoria compartida** para comunicación entre procesos.

### Concurrencia y sincronización

- Desarrollo de programas utilizando **threads**.
- Sincronización mediante **mutex**.
- Coordinación mediante **semáforos**.
- Resolución de problemas relacionados con **race conditions**.
- Exclusión mutua y acceso concurrente a recursos compartidos.
- Análisis de situaciones de **deadlock**.

### Sistemas operativos

También trabajé conceptos relacionados con:

`Processes` · `Threads` · `Scheduling` · `Synchronization` · `IPC` · `Shared Memory` · `Message Queues` · `Pipes` · `Mutex` · `Semaphores`

---

# 🛠️ Stack técnico

<div align="center">

### Lenguajes

[![Languages](https://skillicons.dev/icons?i=ts,js,java,c,html,css)](https://skillicons.dev)

![Prolog](https://img.shields.io/badge/Prolog-74283C?style=for-the-badge)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

### Frontend

[![Frontend](https://skillicons.dev/icons?i=nextjs,react,tailwind)](https://skillicons.dev)

![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white)
![Radix UI](https://img.shields.io/badge/Radix%20UI-161618?style=for-the-badge&logo=radixui&logoColor=white)

### Backend & Data

[![Backend](https://skillicons.dev/icons?i=nodejs,prisma,postgres,supabase)](https://skillicons.dev)

![Neon](https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logoColor=black)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white)

### Servicios

![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=for-the-badge&logo=clerk&logoColor=white)
![Auth.js](https://img.shields.io/badge/Auth.js-000000?style=for-the-badge)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=for-the-badge&logo=resend&logoColor=white)
![Upstash](https://img.shields.io/badge/Upstash-00E9A3?style=for-the-badge&logo=upstash&logoColor=black)

### Testing, deploy y herramientas

[![Tools](https://skillicons.dev/icons?i=vitest,vercel,githubactions,git,github,linux,eclipse)](https://skillicons.dev)

</div>

---

# 🧠 Ingeniería y fundamentos

Más allá de las tecnologías concretas, me interesa entender y aplicar los conceptos que permiten diseñar sistemas mantenibles y robustos.

<div align="center">

`Arquitectura en capas` · `Arquitectura hexagonal` · `Patrones de diseño`

`REST APIs` · `Modelado de datos` · `Multi-tenancy` · `Row Level Security`

`Testing automatizado` · `ADRs` · `UML` · `C4`

`Transacciones` · `Concurrencia` · `Sincronización` · `IPC`

`Procesos` · `Threads` · `Sistemas Operativos`

`Programación lógica` · `Recursión` · `Backtracking`

</div>

---

# 📈 GitHub

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Mellingergaston&show_icons=true&hide_border=true&theme=transparent" />

<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Mellingergaston&layout=compact&hide_border=true&theme=transparent" />

</div>

---

# 📫 Contacto

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Gastón%20Mellinger-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/gaston-mellinger-14997542a/)

[![Email](https://img.shields.io/badge/Email-gaston.mellinger1%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:gaston.mellinger1@gmail.com)

[![GitHub](https://img.shields.io/badge/GitHub-Mellingergaston-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mellingergaston)

[![Zonea](https://img.shields.io/badge/Zonea-zonea.app-10172a?style=for-the-badge&logo=googlechrome&logoColor=white)](https://zonea.app)

</div>

---

<div align="center">

### Building systems, not just interfaces.

</div>
