# Proyecto Colaborativo - Panel de Control SB Admin

## Descripción General
Este repositorio contiene una práctica de simulación de flujo de trabajo colaborativo mediante control de versiones con Git y GitHub. El objetivo principal fue coordinar el desarrollo modular de una interfaz web basada en la plantilla **SB Admin**, dividiendo responsabilidades entre dos desarrolladores y gestionando la integración de características mediante ramas independientes hacia la rama principal.

---

## Integrantes del Proyecto

* **Rosa Cristel Félix Guzmán** — Developer 2 / Administrador del repositorio (Gestión de rama `main`, edición de vistas de tablas y fusión de cambios).
* **Julio César Trujillo García** — Developer 1 (Gestión de rama `developer2`, edición del dashboard principal).

---

## Roles

### 1. Developer 1 (Administrador / Main & Dashboard)
* **Responsabilidad:**
  * Inicialización del repositorio y configuración del entorno base.
  * Implementación y limpieza de la estructura principal (`index.html`).
  * Configuración del menú de navegación lateral (*sidenav*), barra superior (*top navbar*) y pie de página.
  * Limpieza del área de contenido del panel para dejar una plantilla base funcional.
  * Revisión, resolución de dependencias de navegación y ejecución de la fusión final (*merge*) hacia la rama `main`.

### 2. Developer 2 (Módulo de Datos / Tablas)
* **Responsabilidad:**
  * Trabajo aislado en una rama de características (`developer2`).
  * Creación y maquetación de la vista independiente de datos (`tables.html`).
  * Integración de componentes visuales de tablas interactivas con paginación, filtros y ordenamiento.
  * Enlace bidireccional entre la vista de panel principal y la vista de tablas.
  * Publicación de la rama `developer2` en el repositorio remoto para su integración.

---

## Estrategia de Ramas y Fusión (Git Workflow)

1. **`main`**: Rama troncal y de producción que contiene el código estable y consolidado.
2. **`developer1` / `developer2`**: Ramas de trabajo donde cada desarrollador implementa sus cambios de manera aislada sin interferir en el código en producción.
3. **Integración (`merge`)**:
   * El responsable de la rama `main` realiza la integración de los cambios de `developer2` mediante comandos de fusión (`git merge developer2`).
   * Se verifica la integridad de los enlaces cruzados entre `index.html` y `tables.html`.
   * Se sincronizan los cambios definitivos hacia GitHub (`git push origin main`).

---

## Tecnologías y Herramientas Utilizadas

* **Versiones:** Git y GitHub.
* **Estilos:** HTML5, CSS3, Bootstrap 5.
* **Plantilla Base:** Start Bootstrap - SB Admin.
* **Editor de Código:** Visual Studio Code.

---

## Estructura del Proyecto

```text
proyectoColaborativoT/
├── assets/
│   └── demo/
│       └── datatables-demo.js
├── css/
│   └── styles.css
├── js/
│   ├── datatables-simple-demo.js
│   └── scripts.js
├── index.html
├── tables.html
└── README.md
