THE BOX MODEL
- descrie spatiul total al elementului
    - marginea   margin
    - bordura   border
    -spatierea  padding
    -continutul  content

pentru a stabili clar dimensiunea unui element ( cand ii specificam o dimensiune aceasta sa contina si border si padding ) utilizam mereu box-sizing: border-box  ideal la inceputul fisierului css cu * adica sa se aplice tutuor elementelor;

- box-sizing descrie cui i se aplica width si heigh.
- implicit e content-box
- se declara border-box pentru a se adresa partii vizibile.
- border: 2px solid black = dimensiune tip culoare
- border-radius in px - rotunjeste colturile 
- pentru a face un element rotund dam border-radius: 50%
- pentru a incapea textul in rotund putem schimba paddingul
- daca nu avem ce face din css atunci vom mai putea adauga elemente noi si le vom aseza absolut pentru a incerca sa il centram ( position absolut fata de elementul parinte cu position relative) top : 50% se muta continutul la jumatatea elementului si se transforma cu transform: translateY(-50%);
- position relative face referinta pentru position absolute
- top - se refera la inaltimea parintelui
- transform il trimite la inaltimea proprie
- pentru a genera un div cu o clasa punem .nume-clasa si tasta tab
- daca avem text pe o singura linie putem utiliza line-heicht cu dimensiunea exacta a elementuli si se va centra 
- padding margin    - cu o valoare se aplca la toate dimensiunile
                    - 4 valori = top right bottom left
                    - 2 valori = top right (left mosteneste de la right si bottom de la top)
                    - 3 valori = top righ bottom ( left mosteneste de la right)
-!!!!!!!! pt interivuri in zona UI se cere dimensiunile margin si specificitate !!!!!!!!
- margin collapse - daca sunt 2 elemente care au margine (right si left respectiv) atuci se va aplica doar marginea mai mare
- la fel daca copilul si parintele au top si bottom (parinte si last child) se colapseaza marginea mai mica, respectiv marginea copilului iese din parinte. Putem adauga un border transparent pentru a rezolva aceasta problema.
- daca folosim inline-block trebuie sa fim atenti la scrierea textului in html deoarece se va vedea spatiul dintre blockuri


Positioning

- in mod implicit elementele sunt pozitionate static
- pentru a le pozitiona diferit vom da celui de al doilea element position relative
- ca position relative sa functioneze trebuie sa specificam cel putin o dimensiune (tob  left)
- partea vizuala se va muta oriunde dar isi va ocupa inca pozitia lui din randul elementelor.
- pentru miscare in sus si  stanga va fi nevoie de numere negative
- position relative - elementul este pozitionat relativ la pozitia statica a elementului
- position absolute scoate elementul dinrandul lor... 
- position absolute muta elementul relativ la pagina.
- elementul absolut isi ia referinta de la primul ancestor cu pozitie relative
- z-index:
    - axa z- este cea care iese din monitor - 
    - functioneaza doar cu o alta pozitie decat cea statica
    - aduce elementul mai in fata daca are valori pozitive sau mai in spate daca are valori negative
- position fixed - il pune in coltul pagini dar se scroleaza cu continutul;
- pozitia fixed este intotdeauna pozitionat cu referinta de la view port.- fereastra prin care vedem pagina web.
- position fixed si absolute iese din pagina complet -  nu mai conteaza pozitia initiala (statica)
- daca elementul se afla intr-un parinte care are dimensiune specificate atunci height 100% inseamna dimensiunea parintele
- pentru a da unui element (!!!back-drop!!!) width si height view portului atunci com da width si height cu 100vw (100% latimea viewportului)respectiv 100vh (100% inaltimea viewportului);
- chiar si pozitia fixed este supusa z-index;
- pentru a utiliza z-index va trebui sa avem lucrurile intr-un container deci trebuie avuta grija la parintii elementelor
- utilizand un astfel de div care acopera tot atunci nu se mai poate modifica nimic de sub el ( modal*)
- modalul trebuie sa nu permita utilizatorului interactionarea cu siteul si pentru asta se foloseste backdrop

float

- scoate elementele din flow normal elementele floatuite devin marginea browserului si resutul se pozitioneaza ca referinta dupa ele

display
- inline
- none (scoate complet elementul si elibera pozitia
iar visibility hidden ocupa in continuare spatiul dar nu se mai vede - este transparent)
- block

-alte tipuri    - INLINE-BLOCK
                - table table-row table-cell
                - flex
                - grid

tema de facut un modal

