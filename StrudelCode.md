# Código de Strudel
## Integración touch designer con Strudel


``` js
// Strudel example for strudel_visual_router_v2
const { visualid } = createParams('visualid')

setcpm(24.5)

let drum = stack(
  s("oh:1").beat("7", 16).visualid("drum_oh"),
  s("hh").beat("3,7,11,15", 16).visualid("drum_hh"),
  s("cp").beat("1,4,11,15", 16).visualid("drum_cp"),
  s("bd").beat("1,5,9,13", 16).visualid("drum_bd")
).bank("RolandTr909")

$drum: stack(drum, drum.osc())

let guitar = note("<[40 52 ~ 47] [52 ~ 40 47]> <[40 52] 55>")
  .sound("gm_electric_guitar_muted").gain("<0.8 1 0.75>").room(0.3)
  .delay(0.35).delaytime(0.1875).jux(rev).hpf(180)

$guitar: stack(guitar, guitar.osc())

let bass = note("28 [~ 28] ~ [28 31]")
  .sound("gm_acoustic_bass").gain(0.85).decay(0.15)
  .slow(8).room(0.05).orbit(3)

$bass: stack(bass, bass.osc())

// IMPORTANTE: harmony contiene notas simultáneas. Con un solo slot de harmony,
// los eventos simultáneos se consolidan en una sola identidad visual y prevalece
// el evento procesado más recientemente. Para monitorear cada voz, divide los patrones
// en Strudel y utiliza harmony_bass, harmony_mid1, harmony_mid2 y harmony_top.
```
