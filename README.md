
---

# Guía de Estudio: Git y GitHub

## 1. Inicialización y Conexión con GitHub

Pasos para crear un repositorio local desde cero y vincularlo con un repositorio remoto:

```bash
git init                                                    # Crea un repositorio local de Git
git add README.md                                           # Añade el archivo al área de Staging
git commit -m "first commit"                                # Guarda los cambios con un mensaje descriptivo
git branch -M main                                          # Renombra la rama principal a 'main'
git remote add origin https://github.com/isaarizaa/Git-Pruebas-.git # Conecta el repo local con el remoto
git push -u origin main                                     # Sube los cambios y vincula la rama por defecto

```

---

## 2. Las Fases de Git (Áreas de Trabajo)

Git divide el ciclo de vida de los archivos en tres estados principales:

* **Workspace (Directorio de Trabajo):**
* Es tu espacio actual de trabajo donde editas los archivos.
* `git status`: Permite conocer el estado actual y ver qué archivos aún no están rastreados (**Untracked files**).


* **Staging Area (Área de Preparación):**
* Zona intermedia donde preparas los cambios antes de guardarlos oficialmente.
* `git add .`: Añade **todos** los cambios del repositorio actual al Staging.
* **.gitignore:** Archivo especial donde puedes enlistar nombres de archivos o carpetas que Git debe ignorar automáticamente al hacer el `git add`.


* **Local Repository (Repositorio Local):**
* Donde se guardan los cambios de forma permanente mediante commits.
* Cada commit genera un **hash** (identificador único) que permite rastrear la versión y volver a puntos anteriores si es necesario.



---

## 3. Comandos Esenciales de Monitoreo

* `git log`: Muestra el historial completo de los commits realizados.
* `git diff`: Permite ver los cambios realizados en el código **antes** de hacer el `git add`.
* `git diff --staged`: Muestra los cambios que ya están en el Staging pero **aún no** tienen commit.

---

## 4. Flujos de Trabajo Colaborativo

En proyectos en equipo, se trabaja con sincronización remota y ramificación para evitar pisar el código de los demás.

* `git pull`: Trae y fusiona los cambios más recientes del repositorio remoto hacia tu rama local actual.
* **Pull Request (PR):** Solicitud para fusionar (hacer merge) los cambios de tu rama de trabajo hacia una rama principal (como `main`). Aquí suelen ocurrir conflictos de código que deben resolverse manualmente.

---

## 5. Tipos de Ramas Principales (GitFlow)

Organizar las ramas por su propósito ayuda a mantener el orden en proyectos grandes:

* **Main (o Master):** Contiene el código oficial, estable y listo para producción.
* **Develop:** Rama de integración donde se unen las nuevas funcionalidades antes de pasar a producción.
* **Feature:** Ramas temporales para desarrollar características específicas o tareas puntuales (ej. `feature/login`).
* **Release / Hotfix:** Ramas de apoyo para preparar lanzamientos o solucionar errores críticos en producción de manera urgente.

---

## 6. Conceptos y Herramientas Extra

* **Merge Commit:** El registro que se crea en la historia al unir dos ramas de manera tradicional.
* **Git Graph:** Extensión visual excelente para ver el árbol de commits, las ramas y el flujo del proyecto de manera gráfica.

---