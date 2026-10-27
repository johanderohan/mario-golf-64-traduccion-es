# Mario Golf (Nintendo 64) — Traducción al castellano

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Traducción al **castellano de España** de *Mario Golf* (Nintendo 64, Nintendo / Camelot, 1999), desde el inglés de la edición estadounidense.
Se distribuye como **parche XDELTA**; necesitas tu propia copia del juego.

## Estado

Versión **[v1.0 — Menús, ayudas y marcador en castellano](https://github.com/johanderohan/mario-golf-64-traduccion-es/releases/tag/v1.0)**, disponible **en revisión**.

- Banco de **500 entradas** de mensajes, menús, reglas, nombres y torneos: 476 modificadas y 24 conservadas (nombres, tecnicismos, «No», símbolos o datos técnicos).
- Créditos: 138 entradas revisadas, **31 cargos y rótulos traducidos**, con personas y empresas conservadas.
- **75 cadenas o formatos ASCII** adaptados, incluidos Minigolf, estadísticas, guardar, puestos y marcadores.
- **118 recursos gráficos** traducidos, contando sus variantes y fases: menús activos/inactivos, controles, opciones, monedas, resultados y HUD.
- Tildes, eñes y signos de apertura añadidos a las fuentes del juego. Se mantienen las unidades y reglas originales.

### Comprobaciones y límites

Se han recorrido desde partida nueva el menú principal, las siete selecciones de modo de un jugador, Opciones, Récords, ayudas, selección de Minigolf e inicio de Torneo. Se han revisado los controles dibujados, párrafos de ayuda largos, el contador del siguiente campo y letras acentuadas. El guardado y la carga se comprobaron en un proceso nuevo con memoria aislada: al reanudar el hoyo vuelve a su inicio, igual que el original.

La construcción parte del original intacto, conserva los límites de memoria conocidos y relee el binario final para auditar bancos, formatos, fuentes, recursos, punteros y checksum. El parche se reaplica sobre el original y produce exactamente la candidata.

**Quedan pendientes** una partida completa, pruebas completas de los modos de 2 a 4 jugadores, créditos en su recorrido normal, Transfer Pak con Game Boy y consola/flashcart u otros emuladores. La fuente alternativa y los avisos de conexión de Game Boy tienen revisión estática; no se ha ensayado la comunicación. La traducción y la QA están asistidas por IA, **sin revisión humana independiente**.

Se conservan voces y logotipo, nombres propios y tecnicismos habituales del golf, como *drive*, *dormie*, *putt*, *green*, *draw* y *fade*. Algunas estadísticas y nombres usan formas cortas para caber en sus campos, como «G. reg.», «Salv. bún.» y «Castillo Peach». No se ha convertido la distancia a metros ni alterado la física.

## Cómo aplicar el parche

1. Descarga **Mario.Golf.N64.ES.v1.0.xdelta** de [Releases](https://github.com/johanderohan/mario-golf-64-traduccion-es/releases/tag/v1.0).
2. Usa la ROM **USA, revisión 0, en formato .z64 (big-endian)**. Comprueba antes:

   | Original | Valor |
   |---|---|
   | Archivo | `Mario Golf (USA).z64` |
   | Tamaño | 33.554.432 bytes (32 MiB) |
   | MD5 | `903e6929666531d72d05d1e4c522e305` |
   | SHA-256 | `871134c893d5d671ef90c88dfbe98fb20fa20853b3370936a1d09aee6de1beae` |

   Si tu copia es .n64 o .v64, conviértela a .z64 y comprueba de nuevo la huella.
3. Aplica con [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases) o con xdelta3:

   ```bash
   xdelta3 -d -s "Mario Golf (USA).z64" Mario.Golf.N64.ES.v1.0.xdelta "Mario Golf (ES).z64"
   ```

4. Comprueba el resultado: **33.554.432 bytes**, MD5 **`16d99993723f12082de3c5a8b33d670f`**.
5. Carga el resultado. Si el emulador pide el tipo de guardado, selecciona **SRAM de 32 KiB (256 Kbit)**. La cabecera incluye esa indicación para los emuladores que la reconocen.

Cada versión se aplica sobre la **ROM USA original**, nunca sobre otra traducción ni sobre el parche anterior.

SHA-256 del parche: `b56e24b09f57d971df6250a080cb964cec4d58db5601862e2529f77e88949c01`.

## Cambios de v1.0

Primera publicación: menús, ayudas, reglas, estadísticas, controles y marcador de Mario Golf de Nintendo 64 en castellano.
Incluye fuentes con caracteres españoles, revisión de campos de texto, guardado comprobado y 118 recursos gráficos adaptados.

## Créditos y referencias

Proyecto de **johanderohan**, con traducción, herramientas y revisión asistidas por IA. Se han usado las letras y paletas del propio juego.
Referencias técnicas: [mariogolf64](https://github.com/monde-lointain/mariogolf64), [MG64Lib](https://github.com/az64/mg64lib) y los proyectos hermanos de Mario Tennis y Evangelion. QA con parallel-n64 / angrylion. Léxico de golf contrastado con la [RFEG](https://rfegolf.es/aprende-mejora/vocabulario-golf).

## Aviso

Traducción hecha por afición, sin relación con Nintendo ni Camelot. No se distribuyen ROM, BIOS ni el juego: únicamente el parche para modificar una copia propia. Los derechos del juego pertenecen a sus respectivos titulares.
