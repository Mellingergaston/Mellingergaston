<div align="center">

# Hola, soy Gastón Mellinger 👋

### Estudiante de Ingeniería en Sistemas de Información · Desarrollador web full stack · Co-fundador de [Zonea](https://zonea.app)

Construyo productos web de punta a punta: desde los requerimientos y el diseño de la arquitectura hasta el deploy.

[![Zonea](https://img.shields.io/badge/Zonea-zonea.app-10172a?style=for-the-badge&logo=googlechrome&logoColor=white)](https://zonea.app)
![UNS](https://img.shields.io/badge/UNS-4%C2%BA%20a%C3%B1o-1e3a8a?style=for-the-badge)
![Ubicación](https://img.shields.io/badge/Bah%C3%ADa%20Blanca-Argentina-74acdf?style=for-the-badge)

</div>

---

## 🧑‍💻 Sobre mí

- 🎓 Curso el 4º año (2º cuatrimestre) de **Ingeniería en Sistemas de Información** en la Universidad Nacional del Sur. Empecé la carrera en 2023.
- 🚀 Co-fundé y desarrollo **[Zonea](https://zonea.app)**, un software para organizar torneos de pádel que hoy se comercializa a clubes.
- 🏗️ Llevo lo que aprendo en la carrera a proyectos reales: relevamiento de requerimientos, análisis, diseño de arquitectura, patrones de diseño, implementación, testing y deploy.
- 🔭 Soy curioso: sigo de cerca las tecnologías y herramientas nuevas, me gusta aprender cosas distintas y buscar formas de innovar.

---

## ⭐ Proyecto destacado

### 🎾 Zonea: gestión de torneos de pádel

[![Web](https://img.shields.io/badge/Ver%20sitio-zonea.app-10172a?style=flat-square&logo=googlechrome&logoColor=white)](https://zonea.app)
![Estado](https://img.shields.io/badge/Estado-en%20producci%C3%B3n-16a34a?style=flat-square)

Plataforma web para que los clubes organicen torneos de pádel de principio a fin. Reemplaza el trabajo manual del organizador: sortea las zonas según el ranking, asigna los horarios según la disponibilidad de cada pareja y de las canchas, y deja el torneo listo para publicar. La desarrollamos de cero junto a [Lucas Bertone](https://github.com/Lucasbertone02).

**Qué hace**

- 🏆 **Cuatro formatos:** clásico (zonas + llave), americano por parejas, americano individual y ligas con tabla o playoff.
- 🗓️ **Zonas, llaves y horarios automáticos:** cabezas de serie por ranking y armado de la agenda según disponibilidad, canchas, descansos y otros torneos del club. Incluye un optimizador de horarios del fin de semana y un editor visual con drag & drop.
- 📊 **Rankings por club y categoría:** ascensos, historial de puntos y actualización automática al cerrar cada torneo.
- 🔗 **Links públicos sin login:** los jugadores siguen zonas, llaves, resultados y su próximo partido casi en vivo desde el celular.
- 🖼️ **Imágenes para redes:** zonas, llaves y rankings exportados con la identidad visual de cada club, además de planillas PDF para imprimir.
- 📺 **TVs del club:** partidos en juego, resultados, avisos y sponsors en las pantallas del complejo.
- 💳 **Administración de la plataforma:** alta de clubes, planes y facturación.

<details>
<summary><b>🏗️ La ingeniería detrás del proyecto</b></summary>
<br>

- **Proceso:** relevamiento del dominio y de los requerimientos funcionales y no funcionales, decisiones registradas en ADRs, especificaciones por funcionalidad, planificación incremental, auditorías y QA manual.
- **Arquitectura:** monolito modular en capas con el dominio aislado del framework, mediante puertos y adaptadores (estilo hexagonal). ESLint hace cumplir las dependencias entre capas.
- **Patrones de diseño:** Repository, Adapter, Inyección de dependencias, Observer (eventos de dominio), Strategy (criterios de desempate), Value Objects y Factory.
- **Multi-tenant:** PostgreSQL compartido, con aislamiento por club mediante Row Level Security. Las operaciones concurrentes se protegen con transacciones y bloqueos.
- **Algoritmos:** motor propio de asignación de horarios con restricciones, búsqueda y reparación; generación de llaves con byes; fixtures de liga por el método del círculo.
- **Testing:** más de 200 archivos de tests con Vitest (unitarios, casos de uso, contratos de repositorios e integración con la base de datos).

</details>

**Stack:** Next.js · React · TypeScript · Tailwind CSS · shadcn/ui · Prisma · PostgreSQL (Supabase) · Auth.js · Zod · Satori · pdf-lib · Upstash · Resend · Vitest · Vercel

---

## 📂 Otros proyectos

### 🚗 AlquilAutos: ecosistema de alquiler de autos

`Ingeniería de Aplicaciones Web` · `Equipo de 6` · `2026`

Marketplace de alquiler de autos dividido en aplicaciones independientes que se comunican por APIs REST: compradores, propietarios, pagos, entregas, reseñas y un dashboard de métricas. Fue la materia que me dio las bases del desarrollo web: integración entre aplicaciones, APIs, autenticación y bases de datos.

**Mi parte**

- **Seller App** (desarrollador principal): gestión de vehículos con carga de imágenes a Cloudinary, ciclo de vida completo de las reservas (8 estados) con transacciones, ingresos, panel de administración y una API REST para las demás apps. Arquitectura en capas con Repository, Service Layer y Server Actions; roles con Clerk.
- **Analytics Dashboard** (en conjunto): consolida en paralelo las métricas de las cinco apps en KPIs, gráficos, rankings y alertas, con exportación a Excel y PDF.

**Stack:** Next.js · React · TypeScript · Tailwind CSS · Prisma · PostgreSQL (Neon) · Clerk · Zod · Cloudinary · Recharts · ExcelJS · jsPDF · Vercel

[![Seller App](https://img.shields.io/badge/Demo-Seller%20App-000000?style=flat-square&logo=vercel&logoColor=white)](https://proyecto-c-seller-alquilautos.vercel.app/)
[![Repo Seller](https://img.shields.io/badge/Repo-Seller%20App-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IAW-2026/proyecto-c-seller-alquilautos)
[![Analytics](https://img.shields.io/badge/Demo-Analytics-000000?style=flat-square&logo=vercel&logoColor=white)](https://etapa-3-analytics-dashboard-alquila.vercel.app/)
[![Repo Analytics](https://img.shields.io/badge/Repo-Analytics-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/IAW-2026/etapa-3-analytics-dashboard-alquilautos)

### 🗓️ SalePadel: turnero para complejos de pádel

`Arquitectura y Diseño de Software` · `Trabajo en equipo` · `2026`

Aplicación web para reservar canchas y completar partidos. Los jugadores reservan turnos, abren lobbies para sumar jugadores y se evalúan después de jugar; el complejo administra canchas, bloqueos, reservas y reportes semanales.

- Recorrimos el ciclo completo de diseño: requerimientos funcionales y no funcionales, casos de uso, reglas de negocio, estudio de viabilidad, diagramas C4 (contexto, contenedores y componentes), modelo de datos, ADRs y especificación de APIs.
- Arquitectura en capas (rutas → servicios → repositorios) con Repository, Service Layer y Observer para desacoplar las notificaciones mediante eventos.
- Finalización automática de turnos con GitHub Actions, reportes en Excel y PDF, notificaciones por mail, pronóstico del clima con OpenWeather y mapa con Leaflet.

**Stack:** Next.js · React · TypeScript · Tailwind CSS · Radix UI · Prisma · PostgreSQL · Clerk · Nodemailer · Recharts · GitHub Actions · Vercel

[![Demo](https://img.shields.io/badge/Demo-SalePadel-000000?style=flat-square&logo=vercel&logoColor=white)](https://proyecto-turnero-ay-d.vercel.app/)
[![Repo](https://img.shields.io/badge/Repo-SalePadel-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/LautyNahid/proyecto-turnero-AyD)

### 🍄 Super Mario 2D: videojuego en Java

`Tecnología de Programación (TDP)` · `Equipo de 5` · `2025`

Juego de plataformas 2D hecho desde cero en Java. Fue el proyecto que me enseñó a trabajar en equipo: entre los cinco diseñamos el sistema (diagrama de clases, responsabilidades y patrones) antes de implementarlo y probarlo.

- Tres niveles cargados desde archivos de texto, seis tipos de enemigos, power-ups, dos skins, puntaje, ranking y sonido.
- Game loop propio, detección de colisiones por hitboxes y scroll horizontal.
- Patrones State (estados de Mario), Abstract Factory (skins), Visitor (colisiones) y Template Method sobre una jerarquía de entidades.

**Stack:** Java 17 · Swing / AWT · Eclipse

[![Repo](https://img.shields.io/badge/Repo-SuperMario2D-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Mellingergaston/SuperMario2D)

### 🧩 M2 Blocks: juego de puzzle con motor lógico en Prolog

`Lógica para Ciencias de la Computación` · `Trabajo en equipo` · `2025`

Juego web de puzzle en el que se disparan bloques numerados hacia una grilla para combinar los iguales y encadenar combos. Toda la lógica del juego está escrita en Prolog, un lenguaje de programación lógica, y una interfaz en React la consulta a través de SWI-Prolog Pengines.

- **Motor de reglas en Prolog:** combinaciones horizontales, verticales, triples, en L y en T, resueltas en cascada hasta que la grilla se estabiliza, más gravedad invertida por columna.
- **Progresión del juego:** cálculo de nuevos máximos, desbloqueo y retiro de bloques, y generación aleatoria del bloque siguiente según el nivel alcanzado.
- **Interfaz en React:** animación paso a paso de cada combinación, puntaje y combos, modo *hint* que previsualiza la jugada en cada columna y un booster temporal que muestra el bloque siguiente.
- Mi aporte se centró en el motor de reglas en Prolog y en la coordinación del flujo de juego en React.

**Stack:** Prolog · SWI-Prolog Pengines · React · TypeScript · CSS

[![Repo](https://img.shields.io/badge/Repo-M2%20Blocks-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/LCC-DCIC-UNS-2025/proyecto-m2blocks-com-20)

---

## 🛠️ Tecnologías

**Lenguajes**

[![Lenguajes](https://skillicons.dev/icons?i=ts,js,java,html,css)](https://skillicons.dev)
![Prolog](https://img.shields.io/badge/Prolog-74283C?style=for-the-badge)
![SQL](https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white)

**Frontend**

[![Frontend](https://skillicons.dev/icons?i=nextjs,react,tailwind)](https://skillicons.dev)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge&logo=shadcnui&logoColor=white)
![Radix UI](https://img.shields.io/badge/Radix%20UI-161618?style=for-the-badge&logo=radixui&logoColor=white)

**Backend y datos**

[![Backend](https://skillicons.dev/icons?i=nodejs,prisma,postgres,supabase)](https://skillicons.dev)
![Neon](https://img.shields.io/badge/Neon-00E599?style=for-the-badge&logoColor=black)

**Autenticación y servicios**

![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=for-the-badge&logo=clerk&logoColor=white)
![Auth.js](https://img.shields.io/badge/Auth.js-000000?style=for-the-badge)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=for-the-badge&logo=zod&logoColor=white)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=for-the-badge&logo=resend&logoColor=white)
![Upstash](https://img.shields.io/badge/Upstash-00E9A3?style=for-the-badge&logo=upstash&logoColor=black)

**Testing, deploy y herramientas**

[![Herramientas](https://skillicons.dev/icons?i=vitest,vercel,githubactions,git,github,eclipse)](https://skillicons.dev)

**Conceptos que aplico**

`Arquitectura en capas` · `Arquitectura hexagonal` · `Patrones de diseño` · `Programación lógica` · `APIs REST` · `Modelado de datos` · `Multi-tenancy y RLS` · `Testing automatizado` · `ADRs` · `UML y C4` · `Ciclo de vida del software`

---

## 📫 Contacto

<!-- TODO: completar con tus datos y descomentar
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/TU-USUARIO)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:TU-MAIL)
-->
[![GitHub](https://img.shields.io/badge/GitHub-Mellingergaston-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mellingergaston)
[![Zonea](https://img.shields.io/badge/Zonea-zonea.app-10172a?style=for-the-badge&logo=googlechrome&logoColor=white)](https://zonea.app)
