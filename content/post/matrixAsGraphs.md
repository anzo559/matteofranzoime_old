---
title: "È possibile rappresentare una matrice attraverso un grafo?"
date: 2019-07-20T01:11:16+02:00
draft: false
toc: false
tags: ["post"]
author: "anzo559"
---

Prima di concentrarmi sulla domanda presente nel titolo, vorrei fare una premessa. 

Qualche tempo fa, grazie al [blog](https://abouthydrology.blogspot.com) del _Prof. Riccardo Rigon_ - professore ordinario presso il Dipartimento di Ingegneria Civile, Ambientale e Meccanica di Trento, sono venuto a conoscenza di [Math3ma](https://math3ma.com).  
Mat3ma nasce nel 2015 dall'idea di _Tai-Danae Bradley_, una dottoranda in matematica presso il City University of New York, che si occupa principalmente di fisica quantistica e teorica.

Come dottore in ingegneria (anche se mi fa strano dirlo :D) posso affermare che, nonostante mastichi abbastanza bene la matematica, quest'ultima viene utilizzata dagli ingegneri principalmente come mezzo per arrivare ad una soluzione (talvolta) soddisfacente. Questo fatto fa si che veniamo spesso derisi da fisici e matematici, in quanto _"ignoranti"_ nella materia più sofisticata del mondo.
<!--  
Come se non bastasse, con l'avvento del nuovo ordinamento gli studenti sono costretti ad una `corsa contro il tempo e contro i crediti` che spesso porta gli insegnanti a trascurare - o non approfondire - dettagli significativi.  
Secondo la mia opinione, quanto descritto è quello che succede durante i corsi di _analisi matematica_ ad Ingegneria. Non dico che la colpa sia da attribuire solamente al sistema universitario, anzi, sono convinto che molti studenti __non vogliano__ affatto studiare argomenti complessi come quelli matematici.
-->

Ma non è questo l'argomento che voglio trattare quest'oggi.  

 <h3 class='section'>
Ma che cosa è un grafo?
 </h3>

 [![Tipologie di grafo](/images/graph_type.jpeg)](https://medium.com/basecs/a-gentle-introduction-to-graph-theory-77969829ead8)
 <p class='caption'>Tipologie di grafo | Source: <a href="http://medium.com", target = "_blank">medium.com</a></p>

 Un __grafo__ è un insieme di `n` nodi tra loro connessi da `t` tratti (o archi) che possono essere _orientati_ (descritti da una direzione e un verso) o non orientati (di verso arbitrario).  
 Un grafo si differenzia da un "albero" (`tree`) principalmente perché quest'ultimo è definito da un verso; mi spiego meglio: in un albero, *ogni vertice ha un nodo precedente e un nodo successivo* che ne definiscono il *verso*. Inoltre, ogni nodo può avere solamente un nodo, passatemi il termine, "padre" (o genitore). Esiste quindi *uno e uno solo* nodo di partenza (`root`); esiste, quindi, una gerarchia per i nodi. Questo non accade in un grafo, che per come è definito non ha alcun nodo _root_.  
 Elemento che lega le due tipologie appena descritte è il numero di nodi: infatti, un grafo - per essere tale - deve essere formato da **almeno un nodo**, come un albero deve avere come minimo un vertice iniziale.

 Formalmente, un grafo è una coppia ordinata 
 $$
    G = (V, E)
 $$

 dove \\(V\\) è l'insieme di nodi (o _vertices_)
$$ 
    V = \\{v_1, v_2, \dots, v_n\\}
$$
 e \\(E\\) è l'insieme dei tratti (_edges_ o _links_)
 $$
E = \\{e_1, e_2, \dots, e_t\\}
 $$

 Come si può vedere nelle figure seguenti, la differenza tra un grafo non ordinato e uno ordinato è sostanziale.

![Unordered graph](/images/unordered-graph.jpg)
<p class='caption'>Esempio di grafo non ordinato</p>

![Ordered graph](/images/ordered-graph.jpg)
<p class='caption'>Esempio di grafo ordinato</p>

Infatti, il k-esimo tratto che congiunge i nodi \\(i\\) e \\(j\\), per un grafo ordinato, viene scritto come \\(e_k = (v_i, v_j),~i\neq j\\).

<h4 class='section'>Alcune curiosità sulla teoria dei grafi</h4>

La _teoria dei grafi_ vede la luce per la prima volta nel 1736, grazie a __Eulero__. Il matematico svizzero, infatti, risolse il problema dei _sette ponti di Königsberg_ utilizzando quella che sarebbe poi diventata la teoria dei grafi. Eulero si chiedeva se fosse possibile partire e arrivare nello stesso punto della città attraversando tutti i ponti una sola volta.  
Grazie alle basi poste da Eulero, la teoria dei grafi si è evoluta ed è tutt'ora impiegata nella descrizione e nella risoluzione di _reti di acquedotti_ o in algoritmi per il calcolo del percorso (chiuso) più breve tra tutte le città del mondo (più info sulla soluzione potete trovarle [qui](http://www.math.uwaterloo.ca/tsp/world/)).

La teoria dei grafi è - come ogni teoria matematica - descritta da teoremi che non esporrò, per non tediarvi con argomentazioni facilmente reperibili altrove.

<div class='spy'>
    <h3>"è possibile rappresentare una matrice attraverso un grafo?"<br/>La risposta è "sì, si può!"</h3>
</div>

<h3 class='section'>Ma quindi?</h3>

Il titolo descrive alla perfezione ciò che è presente nelle righe che seguono: "è possibile rappresentare una matrice attraverso un grafo?"  
La risposta è "sì, si può!"  
E non solo: è anche possibile derivare una matrice da un grafo.

L'idea di Tai-Danae Bradley è che _ogni matrice può essere rappresentata da un **grafo pesato** "bipartito"_. Per _pesato_ si intende che ad ogni __tratto__ corrisponde una __valore__; mentre, un _grafo bipartito_ (detto anche _bigraph_) è un grafo i cui nodi possono essere suddivisi in due insiemi differenti (e.g. \\(\mathbb{U}\\) e \\(\mathbb{V}\\)) rappresentati con colori diversi.

![Bigraph](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d6/Biclique_K_3_5.svg/330px-Biclique_K_3_5.svg.png)
<div class='caption'>
    Esempio di bigraph | Source: <a href="https://en.wikipedia.org/wiki/Bipartite_graph">Wikipedia</a>
</div>

Per un grafo bipartito, allora vale
$$
    G = (U, V, E)
$$

Ad esempio, per il seguente grafo corrisponde la matrice alla sua sinistra.

![3x2_graph](https://uploads-ssl.webflow.com/5b1d427ae0c922e912eda447/5c7ed363dad0a55aa8223aea_pic2.jpg)
<div class='caption'>
    Esempio di corrispondenza tra matrice e grafo | Source: <a href='https://www.math3ma.com/blog/matrices-probability-graphs'>Math3ma.com</a>
</div>

Le righe della matrice corrispondono ai tre nodi verdi del grafo, mentre le due colonne sono rappresentate dai nodi rossi sulla destra.  
Il valore del lato è così calcolato: si consideri ad esempio l'elemento \\(M_{11}\\) della matrice \\(\underline{\underline{M}}\\); l'elemento si trova sulla _riga_ \\(1\\) e sulla colonna \\(1\\), cioè collega il __primo nodo__ a sinistra (riga \\(1\\)) con il __primo nodo__ a destra (colonna \\(1\\)). Il valore del lato è, appunto \\(-1\\).  
Proseguendo, considerando l'elemento \\(M_{21}\\) - che è posizionato sulla riga \\(2\\) e sulla colonna \\(1\\) e collega il __secondo nodo__ verde con il __primo nodo__ rosso. L'etichetta del tratto considerato è il valore corrispondente a \\(M_{21}\\) (i.e. \\(4\\)).  
Al contrario, i valori nulli della matrice \\(\underline{\underline{M}}\\) significano che non sono presenti tratti che congiungono i nodi in esame.

<div class='spy'>
    <h3>
    Formalmente, una matrice può essere anche vista come una funzione che prende valori da degli insiemi X e Y e riporta valori in R
    </h3>
</div>

<h3 class='section'>Ma perché è possibile questo?</h3>

Formalmente, una matrice \\(\underline{\underline{M}}\\) è un "array" di dimensioni \\(n \times m\\), ma può essere anche vista come una funzione che prende valori da degli insiemi \\(X\\) e \\(Y\\) e riporta valori in \\(\mathbb{R}\\)
$$
    M: X\times Y \longrightarrow  \mathbb{R}
$$

ove
$$
X = \\{x_1, x_2, \dots, x_n\\}~,~ \quad Y = \\{y_1, y_2, \dots, y_m\\}
$$

Allora, l'elemento \\(M_{ij}\\) può essere rappresentato come

$$
    M_{ij} = M(x_i, y_i) , \quad \forall i \in 1, 2, \dots, n~,\quad\forall j = 1, 2, \dots, m
$$
La seguente immagine riassume quanto appena scritto.

![Mij_element](https://uploads-ssl.webflow.com/5b1d427ae0c922e912eda447/5c7eda5fdd9637358da070a1_pic3.jpg)
<div class='caption'>
    Possibile rappresentazione degli elementi della matrice | Source: <a href='https://www.math3ma.com/blog/matrices-probability-graphs'>Math3ma.com</a>
</div>

E questo è tutto per quanto rigurda la rappresentazione di una matrice come grafo.  

<h3 class='section'>Prodotto tra matrici</h3>

I medesimi concetti possono essere applicati al prodotto tra matrici, che corrisponde a _percorrere tutti i possibili percorsi_ che collegano i due nodi.

Si comprende meglio analizzando la seguente figura:

![matrix_multiplication](https://uploads-ssl.webflow.com/5b1d427ae0c922e912eda447/5c7de09a2121fc6c13ed3bd5_pic5.jpg)
<div class='caption'>
    Corrispondenza tra prodotto fra matrici e grafi | Source: <a href='https://www.math3ma.com/blog/matrices-probability-graphs'>Math3ma.com</a>
</div>

Nella figura sono presenti due matrici: \\(\underline{\underline{M}}\\) e \\(\underline{\underline{N}}\\) tali che

$$
    M: X \times Y \longrightarrow \mathbb{R}~,\quad N: Y \times Z \longrightarrow \mathbb{R}
$$

dove in questo caso si ha
\\(X = \\{x_1, x_2, \dots, x_n\\}\\) e \\(Z = \\{z_1, z_2, \dots, z_l\\}\\), essendo i nodi \\(\\{y1, y2, \dots, y_m\\}\\) nodi interni e quindi non ricadenti nel prodotto.

Come ben sapete, il prodotto tra due matrici è un prodotto _riga per colonna_ perciò, il numero di colonne di \\(\underline{\underline{M}}\\) deve corrispondere al numero di righe di \\(\underline{\underline{N}}\\). Guardando la figura sopra riportata si può notare che così è.  
Secondo quanto detto sopra, il primo elemento della __matrice prodotto__ - cioè risultante dal prodotto \\(\underline{\underline{M}}\,\underline{\underline{N}}\\) - è definito come l'etichetta del tratto che congiunge i due nodi \\(x_1\\) e \\(z_1\\)  (vale, quindi, anche l'opposto di quanto detto sopra). Ma in questo caso, i tratti che congiungono i nodi sono molteplici; allora, il valore finale dell'elemento è definito come la somma dei prodotti delle etichette sui lati per ogni percorso; Per il primo elemento si trovano i percorsi \\(\overline{(x_1\,y_1\,z_1)}\\) e \\(\overline{(x_1\,y_2\,z_1)}\\), dove

$$
\begin{aligned}
&\overline{x_1\,y_1} = -1\quad &&\overline{y_1\,z_1} = 5\\
&\overline{x_1\,y_2} = 2 \quad &&\overline{y_2\,z_1} = -7
\end{aligned}
$$

Moltiplicando i termini dei singoli percorsi si ottiene
$$
\overline{(x_1\,y_1\,z_1)} = -1\cdot 5 = -5 \quad \overline{(x_1\,y_2\,z_1)} = 2\cdot -7 = -14
$$

L'elemento \\((M\,N)_{11}\\) è la somma dei prodotti appena calcolati, cioè

$$
    (M\,N)_{11} = -5 - 14 = -19
$$
che corrisponde al valore dell'elemento sulla prima riga e sulla prima colonna della matrice prodotto e quindi al valore del tratto che collega \\(x_1\\) a \\(z_1\\).  
Come si può notare dal grafo a destra, nel grafo risultante i nodi interni \\(Y\\) collassano, ottenendo effettivamente il grafo che corrisponde a una matrice di dimensioni \\(3 \times 2\\).

<h3 class = 'section'>Altre applicazioni</h3>

L'autore prosegue la trattazione descrivendo, ad esempio, le matrici simmetriche e trasposte e i relativi grafi, nonché applicando la teoria descritta ad elementi di probabilità che io non discuterò.

Vi invito comunque a visitare il suo blog per trovare spunti riflessivi particolarmente interessanti ed ampliare le vostre conoscenze matematiche.