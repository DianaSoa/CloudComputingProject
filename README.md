# API Guide

## Introducere
Prezentul document serveste drept documentatie pentru proiectul din cadrul seminarului de Cloud Computing, masteratul SIMPRE, anul I, semestrul II.

## Descriere problema
Aceasta aplicatie a fost construita avand in vedere insasi problema pusa de proiectul pentru care a fost creata. S-a dorit punerea la un loc a resurselor ce pot fi utilizate pentru integrarea unui API, si anume: o lista a API-urilor existente, alaturi de cateva exemple. 
De multe ori, organizarea intr-un singur loc a resurselor necesare poate creste productivitatea si poate duce la o utilizarea adecvata, mai eficienta a timpului. Din experienta proprie, documentarea pentru un proiect poate fi, de multe ori, mai dificila decat construirea proiectului in sine.

## Descriere API
Pentru prima parte a aplicatiei (lista API-urilor), s-a folosit public-api.(1) Acesta pune la dispozitia utilizatorilor o lista cu API-ruile publice existente, impartite pe categorii (ex.: Animals, Health, Cryptocurrency etc.) 
In continuare, au fost construite doua exemple, ce folosesc doua dintre API-urile din lista de mai sus.
Pentru primul exemplu, s-a utilizat randomcat.(2) Acest API ofera utilizatorilor o imagine/gif random cu pisici, la cerere.
Pentru cel de-al doilea exemplu, s-a folosit lyrics.ovh. Pe baza input-ului oferit de utilizator, acest API ofera versuri ale unei melodii a unui artist specificat.

Aplicatia este menita sa ofere celor ce o acceseaza o imagine de ansamblu asupra API-urilor pe care le pot folosi, alaturi de cateva exemple. Exemplele sunt prezentate sub forma de cod, dar pot fi si testate.

## Flux de date

- Request : GET / https://api.publicapis.org/entries,
```
{
    "params" : 
    {
        "category" : "Animals"
    }
}
```
Response:
```
{
    "entries" : 
    {
        "API" : "Cat Facts",
        "Auth" : "",
        "Category" : "Animals",
        "Cors" : "no",
        "Description" : "Daily cat facts",
        "HTTPS" : true,
        "Link" : "https://alexwohlbruck.github.io/cat-facts/"
    },
    etc.
}
```

- Request GET / https://aws.random.cat/meow

Response: 
```
{
    "file" : "https:\/\/purr.objects-us-east-1.dream.io\/i\/img_20161127_133647.jpg"
}
```

- Request GET / https://api.lyrics.ovh/v1/
```
{
    "params" : 
    {
        "artist" : "The Cat Empire",
        "title" : "The Chariot"
    }
}
```
Response:
```
{
    "lyrics" : "This is a song that came upon me
    \nOne night\nWhen the news it had been telling me
    \nAbout one more war and one more fight\n
    And 'aeh' I sighed but then\n
    I thought about my friends\nThen I wrote this declaration\n
    Just in case the world end\n\n
    Our guns\nWe shot them in the things we said\n
    Ah we didn't need no bullets\n'Cause we rely on some words instead\n
    Kill someone in argument\nOutwit them with our brains\n
    And we'd kill ourselves laughing\nAt the funny things we'd say\n\n
    And bombs\nWe had them saved for special times\n
    When the crew would call a shakedown\nWe break down a party landmine\n
    Women that so sexy\nThey explode us with their looks\n
    Ah we blowing up some speakers\nJumping round till the ground shook\n\n
    And missiles\nThey were the roadtrips that we launched\n
    T-t-tripping across this island\nStarting missions at the break of dawn\n
    Yawn and smile say\n'What direction shall we take?'\n\n
    'Somewhere where it warm and wet'\nThis be the route we'd always take and\n\n
    Our weapons were our instruments\nMade from timber and steel\n
    We never yielded to conformity\nBut stood like kings\n
    In a chariot that's riding on a\nRecord wheel\n\nAnd our airforce flying\n
    When the frisbee in the sky\nHave a session while we're smoking\n
    Now we're feeling extra high\nAnd we'd sneak into a carpark\n
    With the skaties on our back\nAnd we're flying down the levels howling\n
    'On the attack now on the attack'\n\nAnd battles\n
    They happened in these dancehalls\nSee we'd rather fight with music\n
    Choosing one the rhythm war\nBattle at these shakedowns\n
    And we battle at these gigs\nWe do battle in our bedrooms\n
    Made some sweet love to the beat\n\nThen our allies grew\n
    Wherever we would roam\nSee whenever we're together\n
    Any stranger feel at home\nIn a way we are an army\n
    But this army not destruct\nNo instead we're doing simple things\n
    Good loving find it run amuck\n\nThis be a declaration\n
    Written about my friends\nIt's engraved into this song\n
    So they know I'm not forgetting them\nSee maybe if the world contained\n
    More people like these\nThen the news would not be telling me\n
    About all that warfare endlessly and\n\nOur weapons were our instruments\n
    Made from timber and steel\nWe never yielded to conformity\n
    But stood like kings\nIn a chariot that's riding on\nA record wheel"
}
```


## Capturi

![Alt text](/PaginaPrincipala.PNG?raw=true "Pagina principala")

## Referinte
(1) https://github.com/davemachado/public-api

(2) https://aws.random.cat/meow

(3) https://lyricsovh.docs.apiary.io/#
