

``` js
setcpm(20)

let drum = stack(
  s("oh:1").beat("7, 13",16).phaser(3).phaserdepth("<.5 .75>"),
  s("hh").beat("3, 7, 11, 15",16),
  s("cp").beat("1, 4, 11, 15",16).duckorbit("2:3").duckattack(0.2),
  s("bd").beat("1, 5, 9, 13",16).room(.9),
).bank("RolandTr909").gain(0.7);

$drum:drum

let guitar = note("36 50 25").sound("gm_electric_guitar_muted");

$guitar : guitar
```
