# Melvin-Web_API

## Week 1

### Dag 1: Woensdag 1 - 4 - 2026
Vandaag was eerste dag van het nieuwe project API. we begonnen klassikaal met een college waarna we in groepjes op zoek gingen naar API's. Ik was er eigenlijk al vrij zeker van op moment dat ik iets wilde gaan doen met games. Dat geeft me namelijk altijd meer motivatie om aan de opdracht te werken. Zo leek het me ook leuk om te gaan kijken naar de web GamePad API. Ik heb tenslotte genoeg controllers om uit te kiezen. Tijdens de workshop van Astro liep ik tegen een paar dingetjes op waar ik niet per se zelf heel veel aan kon doen, maar ze wel op heb weten te lossen. Zo had ik mijn mapje opgeslagen in een mapje met een & teken erin, dat vond de terminal niet zo leuk.   
Voor mijn idee voor de opdracht wilde ik iets gaan doen met de pokémon APIm, ook weer voor meer motivatie en een cooler project daardoor. Mijn idee was dat je op de landingspagina een team kan samenstellen en dat je dan per pokemon ook details kan bekijken. Op die manier voldoe ik dan namelijk al aan een overview en een detailpagina. Maar ik moest nog iets met 2 web API's, Het idee was dat je dan met je gemaakte team kon spelen op een canvas en ze kon besturen met een controller. Het klonk persoonlijk nog niet heel vet. Ik had heb even met Jad overlegd en later ook met Cyd erbij. We kwamen tot het idee om iets te gaan proberen met AR. Als dat zou lukken zou dat heel vet zijn, ik hoop dat het lukt. Het nieuwe AR idee had ik nog niet op papier uitgewerkt, maar alle schetsen die ik had staan hieronder.

<img src="Assets/README_imgs/Schets_LandingPage.jpg" alt="Schets van de landings pagina">
<img src="Assets/README_imgs/Schets_DetailPage.jpg" alt="Schets van de detail pagina">
<img src="Assets/README_imgs/Schets_LoadingPage.jpg" alt="Schets van de loading pagina">
<img src="Assets/README_imgs/Schets_CanvasPage.jpg" alt="Schets van de Canvas pagina">

#### Checkout met Dylan
Ik heb mijn checkout met Dylan online gedaan, omdat ik wat eerder naar huis ging vanwege mijn verkoudheid. Ik kon Dylan nog even helpen met het setuppen van Astro en heb mijn idee uitgelegd wat ik tot nu toe had. Zelf had hij op dat moment nog geen idee voor zijn opdracht.

### Weekverslag
Deze week zijn we begonnen met het API project. Deze week was een beetje kort, hierdoor is er niet heel veel gebeurt. Ik heb deze week een workshop over Astro gevolgd om dat een beetje te leren kennen. Tijdens de workshop waren er een paar problemen, maar die kreeg ik na die tijd opgelost. Ook heb ik een beetje onderzoek gedaan naar verschillende Content en Web API's. Ik ben uitgekomen dat ik iets wil doen met de Pokémon API, omdat dat me veel motivatie geeft. Verder wil ik iets doen met de GamePad en Canvas API's. Gewoon om het zo gamy mogelijk te maken. Als eerste idee had ik dat je een team kon samenstellen en dan met dat een beetje kon spelen / rondlopen op het canvas. Maar dat was nog een beetje simpel. Cyd en Jad hadden geholpen met een ander idee en dat was iets doen met AR. Ik zie nog niet helemaal voor me hoe ik dat ga doen, maar dan komt dan later nog wel. Ik wil wel nog steeeds iets doen met die GamePad API.

### Voortgangsgesprek
Ik had mijn idee gepitched over dat ik iets met AR wilde gaan proberen. Iedereen vond dit eigenlijk wel een heel leuk idee, zelf heb ik dat uiteraard ook. Het gaat alleen wel echt een uitdaging worden om het werken te krijgen. Cyd had ook nog gezegd dat als de AR web API al zou werken, ik misschien niet eens een tweede web API nodig heb. Maar zelf denk ik dat het er vanzelf wel meer worden in de vorm van bijvoorbeeld localstorage of iets dergelijks. Cyd wil in ieder geval een Mewtwo op de ene schouder en een Squirtle op de andere.

### Bekeken bronnen van deze week
https://ar-js-org.github.io/AR.js-Docs/<br>
https://stackblitz.com/edit/pokemon-api?file=index.js<br>
https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API<br>

## Week 2
### Dag 2: Woensdag 8 - 4 - 2026
Beginnen met workshop
Begin gemaakt aan de overview pagina

Vandaag begonnen we met het echt maken van de website. Beginnend met een workshop over Astro. Deze was wel heel handig, heel veel informatie daaruit kon ik daarna namelijk gebruiken voor mijn eigen website. Ik ben vandaag namelijk begonnen met het setuppen van mijn overview pagina. Dit kreeg ik redelijk snel aan de praat. Met de styling ben ik ook al een flink uit gekomen, het is soms alleen nog een beetje onoverzichtelijk in de opbouw van mijn code. Ik had dus ook Jad nog even gevraagd of hij er nog even naar kon kijken. Nu is mijn opbouw in ieder geval goed en kan ik dat aanhouden voor de rest van mijn website. Voor de typings van de pokémon wilde ik de kleuren van de typing gebruiken zoals ze in pokemon zijn. Dit heb ik aan ChatGPT gevraagd. De code die daaruit kwam staat hieronder. Dit was voornamelijk voor de verschillende kleuren, die heb ik later opgeslagen in mijn :root zodat ik ze voor andere styling op de detailpagina ook meteen kan gebruiken.

#### ChatGPT code
Prompt: Could you give me different styling for each typing? So that the background color is different?
```
<div class="types">
  {pokemon.types.map((typeObj) => (
    <span class={`type type-${typeObj.type.name}`}>
      {typeObj.type.name}
    </span>
  ))}
</div>
```
```
/* Type-based colors */
.type-normal { background: #A8A77A; color: #fff; }
.type-fire { background: #EE8130; color: #fff; }
.type-water { background: #6390F0; color: #fff; }
.type-electric { background: #F7D02C; color: #333; }
.type-grass { background: #7AC74C; color: #333; }
.type-ice { background: #96D9D6; color: #333; }
.type-fighting { background: #C22E28; color: #fff; }
.type-poison { background: #A33EA1; color: #fff; }
.type-ground { background: #E2BF65; color: #333; }
.type-flying { background: #A98FF3; color: #fff; }
.type-psychic { background: #F95587; color: #fff; }
.type-bug { background: #A6B91A; color: #333; }
.type-rock { background: #B6A136; color: #fff; }
.type-ghost { background: #735797; color: #fff; }
.type-dragon { background: #6F35FC; color: #fff; }
.type-dark { background: #705746; color: #fff; }
.type-steel { background: #B7B7CE; color: #333; }
.type-fairy { background: #D685AD; color: #fff; }
```


