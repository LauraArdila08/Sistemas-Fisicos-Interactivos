
# UNIT 1 - AUDIO

## 04-Actividad de exploración :musical_score:

Mezcla sonora batería más guitarra más bajo :drum: :guitar: :musical_note:

``` js
setcpm(20)

let drum = stack(
  s("oh:1").beat("7, 13",16).phaser(3).phaserdepth("<.5 .75>"),
  s("hh").beat("3, 7, 11, 15",16),
  s("cp").beat("1, 4, 11, 15",16).duckorbit("2:3").duckattack(0.2),
  s("bd").beat("1, 5, 9, 13",16).room(.9),
).bank("RolandTr909").gain(0.7);

$drum:drum

let guitar = note("<[40 52 ~ 47] [52 ~ 40 47]> <[40 52] 55>")
  .sound("gm_electric_guitar_muted").gain("<0.8 1 0.75>").room(0.3)
  .delay(0.35).delaytime(0.1875).jux(rev).hpf(180).orbit(2)

$guitar: guitar

let bass = note("28 [~ 28] ~ [28 31]")
  .sound("gm_acoustic_bass").gain(0.85).decay(0.15)
  .slow(8).room(0.05).orbit(3)

$bass: bass
```


