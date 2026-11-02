# MLB Power Pros 2008 for Nintendo Switch (homebrew)

Native Nintendo Switch build of the **MLB Power Pros 2008** recompilation (Wii, RL8E54), made with the
[MLBPowerPros2008Recomp](https://github.com/HopeAero/MLBPowerPros2008Recomp) project. It runs at 60 fps in
handheld mode with stock clocks for almost the whole game.

Story, photos and the technical write-up:
[Discussion #8](https://github.com/HopeAero/MLBPowerPros2008Recomp/discussions/8).

**This repository only hosts the Switch releases.** It contains **no game assets**: you need your own copy of
MLB Power Pros 2008 for the Wii (USA, RL8E54). The source code, the recompiler patches and the PC version live in
the main repository ([branch `switch-arm64`](https://github.com/HopeAero/MLBPowerPros2008Recomp/tree/switch-arm64)).

## Requirements

- A Nintendo Switch running custom firmware (Atmosphère) and a homebrew launcher (hbmenu or Sphaira).
- Launch homebrew with **full memory** ("title takeover": hold **R** while opening an installed game, or use a
  forwarder). Album/applet mode does not have enough memory.
- Your own dump of **MLB Power Pros 2008 (Wii, USA, RL8E54)**, either as an ISO or as an extracted disc folder.
- For a 4.7 GB ISO the SD card must be **exFAT** (FAT32 cannot hold files over 4 GB).

## Install

1. Download `MLBPR2008-NX-<version>.zip` from [Releases](../../releases) and copy its `switch` folder to the
   root of your SD card. You get `sdmc:/switch/mlbpowerpros2008/` with `MLBPowerPros2008.nro` and its runtime files.
2. Add your game, one of:
   - **ISO:** copy it as `sdmc:/switch/mlbpowerpros2008/game.iso`. The first start checks it (about half a
     minute, only once).
   - **Extracted disc:** a `Data` folder (with `sys/` and `files/`) in `sdmc:/switch/mlbpowerpros2008/Data`.
3. Open **MLB Power Pros 2008** from the homebrew menu (with full memory). The launcher opens first: pick a
   **graphics preset** and press **PLAY**.

Optional: create a home-menu **forwarder** with Sphaira.

## Graphics presets

| Preset | What it does | Recommended |
|---|---|---|
| **Low** | No player shadows, no reflections, tighter play camera | Stock clocks. 60 fps almost always; brief dips can still appear with bases loaded and long throws to the catcher |
| **Medium** | The original look | Overclock recommended |
| **High** | 1.5x internal resolution | Overclock recommended |

Every option can also be changed on its own in **VIDEO**.

## Mods and saves

- Mods (rosters, uniforms, stadiums, schedules, callnames) go in `sdmc:/switch/mlbpowerpros2008/mods/<mod>/` and are
  enabled in the launcher's **MODS** tab (they apply the next time you open the game). Same format as on PC.
- **Callnames** (new player names for the commentators): make the mod on PC with the Callname Editor (or write
  `callnames/callnames.toml` by hand), copy the mod folder to the SD and enable it. The first start after adding a
  name takes a moment longer while its audio is encoded; later starts use the cache in `UserData/Cache`.
- Saves, settings and logs are in `sdmc:/switch/mlbpowerpros2008/UserData/`.
- Success player passwords: **EXPORT** / **IMPORT** in My Data use `UserData/Players/*.txt`, the same files as on PC.

## Reporting problems

Open an issue in the [main repository](https://github.com/HopeAero/MLBPowerPros2008Recomp/issues) with what you
did, your console mode (handheld/docked, overclock or not) and, if possible, the newest file in
`UserData/Logs/` and `sdmc:/atmosphere/crash_reports/`.

## License

The NRO is built from GPL-3.0 code (see the main repository's `LICENSE`). MLB Power
Pros 2008 is © Konami; this is an unofficial fan project, not affiliated with Konami, MLB or Nintendo.

---

# MLB Power Pros 2008 para Nintendo Switch (homebrew)

Versión nativa para Nintendo Switch de la recompilación de **MLB Power Pros 2008** (Wii, RL8E54), hecha con el
proyecto [MLBPowerPros2008Recomp](https://github.com/HopeAero/MLBPowerPros2008Recomp). Corre a 60 fps en
portátil y sin overclock en casi todo el juego.

Historia, fotos y explicación técnica: [Discussion #8](https://github.com/HopeAero/MLBPowerPros2008Recomp/discussions/8).

**Este repositorio solo aloja los releases de Switch.** **No contiene archivos del juego**: necesitas tu propia
copia de MLB Power Pros 2008 para Wii (USA, RL8E54). El código fuente, los parches del recompilador y la versión de
PC están en el repositorio principal ([rama `switch-arm64`](https://github.com/HopeAero/MLBPowerPros2008Recomp/tree/switch-arm64)).

## Requisitos

- Una Nintendo Switch con firmware personalizado (Atmosphère) y un lanzador homebrew (hbmenu o Sphaira).
- Abrir el homebrew con **toda la memoria** (mantén **R** al abrir un juego instalado, o usa un forwarder). El modo
  álbum no tiene memoria suficiente.
- Tu propia copia de **MLB Power Pros 2008 (Wii, USA, RL8E54)**, como ISO o como carpeta del disco extraída.
- Para una ISO de 4,7 GB la SD tiene que estar en **exFAT** (FAT32 no admite archivos de más de 4 GB).

## Instalación

1. Descarga `MLBPR2008-NX-<versión>.zip` de [Releases](../../releases) y copia su carpeta `switch` a la raíz de la
   SD. Queda `sdmc:/switch/mlbpowerpros2008/` con `MLBPowerPros2008.nro` y sus archivos del runtime.
2. Añade tu juego, de una de estas formas:
   - **ISO:** cópiala como `sdmc:/switch/mlbpowerpros2008/game.iso`. El primer arranque la comprueba (medio minuto
     más o menos, solo una vez).
   - **Disco extraído:** una carpeta `Data` (con `sys/` y `files/`) en `sdmc:/switch/mlbpowerpros2008/Data`.
3. Abre **MLB Power Pros 2008** desde el menú homebrew (con toda la memoria). Primero sale el launcher: elige un
   **perfil gráfico** y pulsa **JUGAR**.

Opcional: crea un **forwarder** en el menú HOME con Sphaira.

## Perfiles gráficos

| Perfil | Qué hace | Recomendado |
|---|---|---|
| **Bajo** | Sin sombras de jugadores, sin reflejos, cámara de jugada más cerrada | Relojes de fábrica. 60 fps casi siempre; puede haber caídas breves con bases llenas y lanzamientos largos al catcher |
| **Medio** | El aspecto original | Se recomienda overclock |
| **Alto** | Resolución interna 1,5× | Se recomienda overclock |

Cada opción también se puede cambiar por separado en **VIDEO**.

## Mods y partidas

- Los mods (rosters, uniformes, estadios, calendarios, callnames) van en `sdmc:/switch/mlbpowerpros2008/mods/<mod>/` y se
  activan en la pestaña **MODS** del launcher (se aplican la próxima vez que abras el juego). Mismo formato que en PC.
- **Callnames** (nombres de jugador nuevos para los comentaristas): crea el mod en PC con el Editor de callnames (o
  escribe `callnames/callnames.toml` a mano), copia la carpeta del mod a la SD y actívalo. El primer arranque tras
  añadir un nombre tarda un poco más mientras se codifica su audio; los siguientes usan la caché de `UserData/Cache`.
- Partidas, ajustes y logs están en `sdmc:/switch/mlbpowerpros2008/UserData/`.
- Contraseñas de jugadores de Success: **EXPORT** / **IMPORT** en My Data usan `UserData/Players/*.txt`, los mismos
  archivos que en PC.

## Reportar problemas

Abre un issue en el [repositorio principal](https://github.com/HopeAero/MLBPowerPros2008Recomp/issues) con qué
hiciste, el modo de la consola (portátil/dock, con o sin overclock) y, si puedes, el archivo más nuevo de
`UserData/Logs/` y de `sdmc:/atmosphere/crash_reports/`.

## Licencia

El NRO se compila a partir de código GPL-3.0 (ver `LICENSE` del repositorio principal). MLB Power Pros 2008 es © Konami; esto es un proyecto no oficial de fans, sin relación con Konami, MLB ni
Nintendo.
