# Grid css
### exemplul de la fireship pentru tema cu flex

- css grid-garden - joc pentru exersare
- display:grid - imparte containerul in cate patratele vrem si punem continutul in ce patratica vrem
- grid-template-columns: 100px 100px 100px - specificam 3 coloane de 100px width
        - este un grid explicit
        - rowrile sunt create implicit in functie de continut
        - daca setam o coloana pe auto ea se va extinde pe tot spatiul disponibil
        - grid-template-columns: repeat(5,100px) (in loc sa specific eu de 5 ori 100 px atunci dam functia repeat)
- grid-template-rows - pentru randuri
    - se poate folosi si repeat
    - grid-auto-rows:150px - ataca randurile create implicit

    - se pot pune oricate repeaturi dorim despartite de spatiu
            - fie asa repeat(5, 5px 100px) si creaza 5 perechi de randuri/coloane primul e 5 si al doilea de 100


- grid-gap: 20px - distanta dintre elemente de 20px 
    - creaza grid tracks (randuri de spatiu intre coloane respectiv randuri)
- grid-auto-flow - elementele care nu incap in primul rand cu nr de coloane dat se muta automat pe urmatorul rand (creaza rand implicit)
    - putem da grid-auto-flow: column (by default e row)- si se va duce automat creaind o noua coloana

-fr unit fraction = ce pondere va lua x element din dimensiunea disponibila

-sizing elements - grid-column: span 2 ( sa se intinda pe 2 celule exact ca la tabel)
    - daca nu incape pe linia pe care este va trece automat pe urmatoara linie pe care incape , in urma lui ramanand spatiu gol
    - daca nu incape nici pe urmatoarea linie se va crea automat o noua coloana implicita ( de dimensiune implicita) 
       - prtea negativa e ca tot ce vine dupa elementul modificat cu span ca fi afisat diferit fiind fortat sa incapa in spatiul nou creat in coloana implicita
- grid-column-start: 1 ; grid-column-end: 4 ( incepe la 1 se termina la 4)
sau
    - grid-column: 1/-1 ( incepe la prima se termina la ultima coloana)
- grid-row: span 2;


- putem verifica daca se poate utiliza  o anumita proprietate pe canIuse

- grid-template-columns: repeat(auto-fill , 300px) - pune automat tot atatea coloane cate incap in ecran 
- grid-template-columns: repeat(auto-fit , minmax(150px, 1fr) )-  coloana nu va ptea fi mai mica decat valoarea declarata dar maxim va putea avea 1 parte din spatiul liber existent

- auto fit si auto fill functioneaza doar pt coloane 


    - va tine cont doar de dimentsiunea containerului nu si de dimensiunea continutului
    -  daca are 599px width atunci vor fi 3 coloane iar elementul 4 va fi pe randul 2
    - daca are 600px atunci textul poate face overflow dar vor fi 4 coloane
- grid-template-areas:
{
    "header1 header1  header1"
    "nav     main     aside"
    ".       main     aside"
    "footer footer  footer"
}

header{ ->elementul header 
    grid-area: header1 ->va avea alocat spatiul header1
}

- auto flow: dense
        - grid-auto-flow: dense - se va ocupa spatiul lasat gol in urma span ului
- justify-items : strech (default) - la dimensiunea containerului indiferent de continut
- justify-items : center (dimensiunea containerului va fi exact cat continutul si centrat sau end sau start)
- align-items: center (default??) - centreaza continutul elementului pe verticala (exista si start si end  si strech - extinde pe toata inaltimea containerului)
- jstify-content : start (default) - mai exista si end, center ( se muta complet coloanele)
    - justify-content : space-around - da spatiu distribuit egal intre toate coloanele adauga un grid track inainte si dupa fiecare coloana
    - justify-content : space-between - imparte spatiul ramas in mod egal intre coloane
- align-items - este exact la fel ca justify-content doar ca pe verticala
- justify-self si align-self (aceleasi valori ca la justify-content si align-content)


