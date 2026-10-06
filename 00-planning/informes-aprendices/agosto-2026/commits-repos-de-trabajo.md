# Informe 2 — Commits en los repositorios en los que trabajaste

**Periodo:** del 1 al 30 de agosto de 2026 (hora Colombia, UTC-5)
**Repositorio principal de la ficha:** https://github.com/code-sena/ADSO-3145556

| Campo | Valor |
|---|---|
| Aprendiz | Juan Esteban Cortes Parra|
| Usuario de GitHub | Juan-Cortes2045|
| Ficha | ADSO-3145556 |
| Proyecto (equipo) | Energy Monitor|
| Correo(s) con el que haces commit | juanestebanp171@gmail.com|
| Fecha de elaboración | 06-10-2026|

<details>
<summary><strong>Instrucciones — léelas y borra este bloque antes de entregar</strong></summary>

**Qué reporta este informe.** Todos los commits que hiciste en **los demás repositorios en los que trabajaste**: tu repositorio personal o de perfil, tu fork de `ADSO-3145556`, repositorios de otros equipos, `design-software` y cualquier otro. **No repitas aquí** los repositorios de tu equipo (`-docs`, `-api`, `-app`, `-db`, `-portal`, `-worker`): esos van en el Informe 1.

**Tipos de repositorio** (úsalos en la columna *Tipo*): `Personal` · `Fork de la ficha` · `Otro equipo` · `design-software` · `Otro`.

**Paso 1 — descubre en qué repositorios trabajaste.** Elige una de las dos formas (reemplaza `TU_USUARIO`):

- *Desde el navegador:* abre
  `https://github.com/search?q=author%3ATU_USUARIO+author-date%3A2026-08-01..2026-08-30&type=commits`
  y mira en qué repositorios aparecen tus commits.
- *Desde la terminal* (requiere `gh`, la CLI de GitHub, con sesión iniciada):

```bash
gh search commits --author=TU_USUARIO --author-date=2026-08-01..2026-08-30 --limit 1000 \
  --json repository --jq '.[] | .repository.fullName' | sort | uniq -c
```

Te devuelve cada repositorio con el número de commits que encontró.

> **Advertencia:** la búsqueda de GitHub solo revisa la **rama por defecto** de cada repositorio. Si trabajaste en otra rama (`dev`, `docs`, `feature/…`), esos commits no aparecen. Por eso el Paso 2 es obligatorio, y además debes acordarte de los repositorios donde trabajaste solo en ramas secundarias.
> Los commits de los días 1 y 30 pueden cambiar de lado por la zona horaria: verifícalos con el Paso 2.

**Paso 2 — obtén los commits de cada repositorio.** Para cada repositorio, desde una terminal **Git Bash**, dentro de tu clon:

```bash
# Ajusta solo estas tres líneas
AUTOR="tu-correo@ejemplo.com"                 # varios correos: "uno@x.com\|otro@y.com"
DESDE="2026-08-01T00:00:00-05:00"
HASTA="2026-08-30T23:59:59-05:00"

URL=$(git remote get-url origin | sed -E 's#^git@github.com:#https://github.com/#; s#\.git$##')
git fetch --all --prune -q
git log --all --no-merges --author="$AUTOR" --since="$DESDE" --until="$HASTA" \
  --date=iso --reverse \
  --pretty=tformat:"| [%h]($URL/commit/%h) | %ad | %s |" | tee commits.md | wc -l
```

- Se imprime **el total de commits**. Las filas ya vienen en formato de tabla y quedan en `commits.md`: ábrelo, copia las filas y pégalas en la tabla del repositorio. Luego borra `commits.md`.
- `--all` incluye **todas las ramas**. Un commit que esté en varias ramas se cuenta una sola vez.
- `--no-merges` deja por fuera los commits de fusión.
- Si el mensaje de un commit contiene el carácter `|`, reemplázalo por `/` para no romper la tabla.
- El enlace de cada commit funciona con el `URL` del repositorio **desde el que clonaste**. Si clonaste un fork, el enlace apunta a tu fork, que es lo correcto.

**Repositorios privados.** Si un repositorio es privado, indica en *Visibilidad* si el usuario `ariel5253` tiene acceso. Un commit que el instructor no puede abrir no se puede verificar.

**Qué cuenta como commit tuyo.** Solo los hechos con tu cuenta. Abre un commit en GitHub: si aparece tu foto de perfil, está vinculado. Si no aparece, tu correo de `git config user.email` no está vinculado a tu cuenta: anótalo en *Observaciones*, no lo ocultes.

**Copia el bloque de la sección 2 una vez por cada repositorio.** Si en el periodo trabajaste en un solo repositorio, deja un solo bloque.

</details>

## 1. Resumen de repositorios

| # | Repositorio | Enlace | Tipo | Visibilidad | Commits |
|---|---|---|---|---|---|
| 1 | `Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico` | https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico.git | Personal| Público  | 55 |
| 2 | `Juan-Cortes2045/Energy-Monitor-application`| https://github.com/Juan-Cortes2045/Energy-Monitor-application.git| Personal| Público| 180|
| 3 | `angelgarcia0/Energy-Monitor-Mobile`| https://github.com/angelgarcia0/Energy-Monitor-Mobile.git| Personal| Público| 75|
| 4 | `Juan-Cortes2045/energy-monitor-backend`| https://github.com/Juan-Cortes2045/energy-monitor-backend.git| Personal| Público| 104|
| | **Total** | | | | **414** |

## 2. Detalle por repositorio

### 2.1 `Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico`

- **Enlace del repositorio:**https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico.git
- **Tipo:** Personal
- **Visibilidad:** Público  (¿`ariel5253` tiene acceso? Sí)
- **Total de commits en el periodo:** 8
- **Qué hice (2 a 3 líneas):** Durante estos commits actualicé y reestructuré el modelo entidad-relación y el diagrama de clases del proyecto, incluyendo la normalización a 3FN y la división del sistema en módulos. También rediseñé el módulo de seguridad con sesiones, configuración y roles, y mantuve actualizado el diccionario de datos con las entidades, atributos, restricciones y relaciones del modelo.

| Commit ID | Fecha y hora | Mensaje |
|---|---|---|
| | | |
| [48fdc53](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/48fdc53) | 2026-05-11 07:08:20 -0500 | modificacion en el MER en la entidad User-telefono nullable |
| [e1743b2](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/e1743b2) | 2026-08-10 22:44:31 -0500 | docs(er-diagram): restructure MER and class diagram for updated system design |
| [0f70d17](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/0f70d17) | 2026-08-11 06:29:51 -0500 | Conflict resolution for local and remote divergent branches |
| [8bd7631](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/8bd7631) | 2026-08-13 14:07:28 -0500 | feat(mer): security module, division into modules, 3FN normalization, and rename Project→Home |
| [ed76b80](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/ed76b80) | 2026-08-20 16:51:19 -0500 | refactor(mer): redesign the security module — UserSession, config, and policies; simplified RBAC |
| [01ac353](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/01ac353) | 2026-08-21 13:47:49 -0500 | docs(classDiagram): Update the class diagram with the new security framework |
| [50f23aa](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/50f23aa) | 2026-08-26 14:11:05 -0500 | Align the data dictionary with the current entity relationship model, including entities, attributes, constraints, data types, and relationships |
| [cf2bd4d](https://github.com/Juan-Cortes2045/Documentacion-proyecto-Monitor-de-consumo-electrico/commit/cf2bd4d) | 2026-08-26 14:19:30 -0500 | chore: delete LibreOffice temporary file |


### 2.2 `Juan-Cortes2045/Energy-Monitor-application`

- **Enlace del repositorio:** https://github.com/Juan-Cortes2045/Energy-Monitor-application.git
- **Tipo:** Personal
- **Visibilidad:** Público(¿`ariel5253` tiene acceso? Sí)
- **Total de commits en el periodo:** 6
- **Qué hice (2 a 3 líneas):** Realicé varias mejoras y refactorizaciones en el frontend, actualizando el concepto de Project a Home y reorganizando el sistema de estilos para usar variables CSS. También implementé los umbrales diarios y mensuales con cálculo automático, mejoré los colores de estados según el tema y eliminé componentes que ya no se utilizaban.

| Commit ID | Fecha y hora | Mensaje |
|---|---|---|
| | | |
| [6e69429](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/6e69429) | 2026-08-25 07:33:25 -0500 | refactor: rename all Project references to Home across files, directories, components and i18n |
| [d94718d](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/d94718d) | 2026-08-25 10:46:26 -0500 | refactor: remove JS design tokens and use CSS variables exclusively |
| [a96756a](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/a96756a) | 2026-08-25 11:04:01 -0500 | chore: remove unused Spinner component |
| [16da997](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/16da997) | 2026-08-25 13:47:15 -0500 | feat: add daily/monthly toggle for thresholds with auto-calculation |
| [710d99f](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/710d99f) | 2026-08-29 11:19:02 -0500 | feat(theme): add danger/success/warning soft+text color variants per theme |
| [c88cc63](https://github.com/Juan-Cortes2045/Energy-Monitor-application/commit/c88cc63) | 2026-08-29 11:19:12 -0500 | fix: replace hardcoded status colors with theme CSS variables across dashboard components |

### 2.2 `angelgarcia0/Energy-Monitor-Mobile`

- **Enlace del repositorio:** https://github.com/angelgarcia0/Energy-Monitor-Mobile.git
- **Tipo:** Personal
- **Visibilidad:** Público(¿`ariel5253` tiene acceso? Sí)
- **Total de commits en el periodo:** 0
- **Qué hice (2 a 3 líneas):**

| Commit ID | Fecha y hora | Mensaje |
|---|---|---|
| | | |

### 2.2 `Juan-Cortes2045/energy-monitor-backend`

- **Enlace del repositorio:** https://github.com/Juan-Cortes2045/energy-monitor-backend.git
- **Tipo:** Personal
- **Visibilidad:** Público(¿`ariel5253` tiene acceso? Sí)
- **Total de commits en el periodo:** 0
- **Qué hice (2 a 3 líneas):**

| Commit ID | Fecha y hora | Mensaje |
|---|---|---|
| | | |


## 3. Verificación del aprendiz

- [x] Todos los commits listados los hice con mi cuenta (aparece mi foto de perfil en GitHub).
- [x] Incluí los commits de **todas las ramas** de cada repositorio, no solo de la rama por defecto.
- [x] Todos los commits caen entre el 1 y el 30 de agosto de 2026 (hora Colombia).
- [x] No repetí repositorios del Informe 1 (los de mi equipo).
- [x] Cada enlace de repositorio y de commit abre en GitHub.
- [x] El total de cada repositorio coincide con el número de filas de su tabla.
- [x] En los repositorios privados indiqué si el instructor tiene acceso.

## 4. Observaciones

*Declaro que la información de este informe es veraz y que los commits listados son de mi autoría.*

**Aprendiz:** Juan Esteban Cortes Parra  **Fecha:** 06-10-2026
