# TypeScript

Inona no atao hoe typescript?

Ny typescript dia language nivoaka tamin'ny février 2012 , izay nokarohin'ny concepteur an' langage C# (Microsoft) dia tsy iza izany fa i Anders Hejlsberg ,
Ny tena tanjona dia ny hahamora ny fanoratana ny Javascript nefa kosa tena fiable amin'ireo projet lehibe.

Inona no tombony amin'ny fampiasana ny TypeScript?

Ny tombony dia mora kokoa ny fampifandraisana ny javascript amin'izay typen'ny donné rehetra raisiny?

**Variable :** 

Ohatra :
```
var enyNaTsia : boolean,
var hafatra : string,
var laharana : number,
var resaka : any
```

**Fonctions :**

Ny typescript dia afaka mi-improvise izay return avoakan'ny function anankiray , izany hoe afaka omenao type izay résultat farany ho avoakan'ilay fonction nataonao

Ohatra:
```
function manisa (n:number) : number (){
  return 70 * n
}
```

**Class sy intérface**

Tsy dia mifanalavitra loatra amin'ny langage de programmation rehetra hainao hatramin'izay ny typage class amin'ny typescript 

Ohatra: 
```
Class Olona {
  kristianina = 100; 
  constructor(isany : number){
    this.kristianina = isany;
  }
  
  manisa(fanisana:number) : number {
    return fanisana;
  }
}

let izaho = new Olona(1);

```

Amin'ny maha Class azy dia afaka manao héritage ihany koa ianao amin'ny alalan'ny mots magique extends 

Ohatra: 

```
class vahoaka extends Olona{
  /// afaka manisy construncteur ianao amin'ny alalan'ny
  super(){}
  ...
  silamo : isa;
}
```

Intérfaces

Ohatra: 
```
interfaces olona {
  mpivavaka : number;
}
```

Izany hoe raha atambatra dia :

```
class vahoaka extends Olona {
  silamo : isa;
}

interfaces olona {
  kristianina : number;
}

var malagasy : Olona = { silamo : 50 , kristianina : 50 };
```


