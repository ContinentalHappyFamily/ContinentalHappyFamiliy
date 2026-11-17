# ♠♥ Continental · Happy Family

App web para apuntar las partidas de Continental de la familia y llevar la clasificación.
Gana quien **menos** puntos tiene.

- **Reglas:** pestaña 📖 con las normas del juego (CA/ES) y el PDF original en `docs/`.
- **Idioma:** català o castellano (cada uno elige el suyo, botón CA/ES arriba).
- **Jugadores:** Joan, Mercè, Albert, Ricard, Cristina L. y Cristina A. (se pueden renombrar y añadir más en *Ajustes*).
- **Jornadas:** fecha + quién juega (casillas ✔). En una jornada se pueden jugar varias partidas (partida 1, 2, 3…).
- **Partidas de 9 rondas:**
  1. 2 tríos
  2. 1 trío y 1 escalera
  3. 2 escaleras
  4. 3 tríos
  5. 2 tríos y 1 escalera
  6. 1 trío y 2 escaleras
  7. 3 escaleras
  8. 4 tríos
  9. 4 escaleras
- **Cerrar con −10:** quien cierra poniendo su última carta en una combinación de la mesa se apunta −10 (botón «−10» al anotar).
- **Borrar partidas vacías:** se guarda la hora de creación de cada partida; si pasa más de 1 hora sin ninguna ronda anotada, se puede borrar.
- **Terminar antes:** al terminar la ronda 7 (y la 8) la app pregunta si se termina la partida o se sigue (también hay un botón).
- **Puntuación:** cualquiera puede anotar. Se pide confirmación y, una vez confirmada, la ronda **no se puede modificar**.
- **Clasificación:** una por cada grupo de jugadores y una general (puntos totales ÷ partidas jugadas), con filtro por año. Solo cuentan las partidas terminadas.
- Sin contraseñas: cada uno elige "¿Quién eres?" y queda registrado quién anotó cada ronda.

## Dónde se guardan los datos

En este mismo repositorio, en `data/continental.json`. Cada ronda anotada es un *commit*, así que hay historial completo de todo.

## Puesta en marcha (una sola vez)

### 1. Subir los ficheros
Sube `index.html`, `README.md` y la carpeta `data/` a la raíz del repositorio `ContinentalHappyFamiliy` (botón **Add file → Upload files**).

### 2. Activar GitHub Pages
Repositorio → **Settings → Pages** → *Source*: **Deploy from a branch** → Branch **main** / carpeta **/(root)** → *Save*.
Al cabo de un minuto la app estará en:
`https://<nombre-de-la-organización>.github.io/ContinentalHappyFamiliy/`

> Con una cuenta gratuita, GitHub Pages necesita que el repositorio sea **público**.

### 3. Crear la clave para poder anotar
Sin clave la app funciona en **solo lectura**. Para poder anotar puntos:

1. GitHub → tu foto → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. *Resource owner*: la organización. *Expiration*: la que quieras (p. ej. 1 año).
3. *Repository access*: **Only select repositories** → `ContinentalHappyFamiliy`.
4. *Permissions → Repository permissions → Contents*: **Read and write**.
5. Genera y copia el token (`github_pat_…`).

> Si la organización lo pide, apruébalo en Organización → **Settings → Personal access tokens → Pending requests**.

### 4. Vincular los móviles
- Abre la app → **Ajustes** → pega el token en *Clave de acceso* → **Guardar y conectar**.
- Aparecerá un **enlace para vincular a otro familiar**: envíalo por WhatsApp. Quien lo abra queda vinculado al momento.
- En el móvil: *Compartir → Añadir a pantalla de inicio* para tenerla como una app.

**Seguridad:** el token solo da permiso sobre este repositorio. No compartas el enlace fuera de la familia. Si se filtra, bórralo en GitHub y crea uno nuevo.

## Instalar en el móvil como una app

**iPhone (Safari):** abre la app en Safari → botón **Compartir** (cuadrado con flecha) → **Añadir a pantalla de inicio** → Añadir.
Después abre la app desde el icono, ve a **Ajustes** y pega el enlace de vinculación en *Clave de acceso o enlace* (en iPhone la app instalada no comparte datos con Safari).

**Android (Chrome):** abre la app en Chrome → menú **⋮** → **Instalar aplicación** (o *Añadir a pantalla de inicio*). Si se abrió antes el enlace de vinculación en Chrome, ya queda vinculada.
