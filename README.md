# Tips for airma.sh

## Useful links

* [Original game](https://airma.sh)
* [Theme on reddit](https://www.reddit.com/r/airmash/)
* [StarWarsMod4AirMash](https://github.com//molesmalo/StarWarsMod4AirMash)
    * [StarMash v2.2 - Extensions Update!](https://www.reddit.com/r/airmash/comments/84jaez/starmash_22_extensions_update_now_released)
    * [StarMash Mod v2 - VANILLA FLAVOUR](https://www.reddit.com/r/airmash/comments/7ydagu/starmash_mod_v2_vanilla_flavour/)
* [StarMash Extensions & Themes tutorials](https://www.reddit.com/r/airmash/comments/86ac48/starmash_extensions_themes_tutorials/)
* [Python client API for Airma.sh](https://github.com/Gadgetoid/python-airmash)

## In-game abilities

### Custom flags

Type `/flag FLAGNAMEHERE`

* `communist`
* `confederate`
* `imperial`
* `rainbow`
* `jolly`

### Emotions

Emotes available: 

* `/tf`
* `/pepe`
* `/clap`
* `/lol`
* `/bro`
* `/kappa`
* `/cry`
* `/rage`

## Other

### Fixing prowler in CTF game

* [Original post](https://www.reddit.com/r/airmash/comments/81fx2l/mitigating_the_opaque_prowler_bug_ctf_v102/dv34r8x/)

```
!function(){
    let Players_reteam = Players.reteam;
    Players.reteam = function(data) {
        Players_reteam.call(Players, data);

        // fix the missing reassignment of game.myTeam
        if (data.id == game.myID)
            game.myTeam = data.team;
    };
}();
```

### Invisible name

You will need to use Unicode:

* [U+2061](https://unicode-table.com/en/2061/)
* [U+2062](https://unicode-table.com/en/2062/)
* [U+2063](https://unicode-table.com/en/2063/)
* `ru`[Some more info](https://habrahabr.ru/post/311518/)

### Zoom-out

* [Original theme](https://www.reddit.com/r/airmash/comments/85yp16/how_to_zoom_out_scalingfactor/)
* code: `javascript:(()=>{config.scalingFactor = 3500;Graphics.resizeRenderer(window.innerWidth,window.innerHeight);})()`
