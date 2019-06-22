---
title: "E` possibile rappresentare una matrice attraverso un grafo?"
date: 2019-06-22T14:47:24+02:00
draft: false
toc: false
tags: ["post"]
author: "anzo559"
---

<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
});
</script>
<script type="text/javascript" async src="path-to-mathjax/MathJax.js?config=TeX-AMS_CHTML"></script>

Prima di concentrarmi sulla domanda presente nel titolo, vorrei fare una premessa. 

Qualche tempo fa, grazie al [blog](https://abouthydrology.blogspot.com) del _Prof. Riccardo Rigon_ - professore ordinario presso il Dipartimento di Ingegneria Civile, Ambientale e Meccanica di Trento, sono venuto a conoscenza di [Math3ma](https://math3ma.com).  
Mat3ma nasce nel 2015 dall'idea di _Tai-Danae Bradley_, una dottoranda in matematica presso il City University of New York, che si occupa principalmente di fisica quantistica e teorica.

Come dottore in ingegneria (anche se mi fa strano dirlo :D) posso affermare che, nonostante mastichi abbastanza bene la matematica, quest'ultima viene utilizzata dagli ingegneri principalmente come mezzo per arrivare ad una soluzione (talvolta) soddisfacente. Questo fatto fa si che veniamo spesso derisi da fisici e matematici, in quanto _"ignoranti"_ nella materia più sofisticata del mondo.  
Come se non bastasse, con l'avvento del nuovo ordinamento gli studenti sono costretti ad una `corsa contro il tempo e contro i crediti` che spesso porta gli insegnanti a trascurare - o non approfondire - dettagli significativi.  
Secondo la mio opinione, quanto descritto è quello che succede durante i corsi di _analisi matematica_ ad Ingegneria. Non dico che la colpa sia da attribuire solamente al sistema universitario, anzi, sono convinto che molti studenti __non vogliano__ affatto studiare argomenti complessi come quelli matematici.

Ma non è questo l'argomento che voglio trattare quest'oggi.  

 <h3 style="text-transform:uppercase">
Ma che cosa è un grafo?
 </h3>

 [![Tipologie di grafo](/images/graph_type.jpeg)](https://medium.com/basecs/a-gentle-introduction-to-graph-theory-77969829ead8)
 <p align="center"><strong>Tipologie di grafo</strong> | <i>Source: <a href="http://medium.com", target = "_blank">medium.com</a></p>

 Un __grafo__ è un insieme di `n` nodi tra loro connessi da `t` tratti (o archi) che possono essere _orientati_ (descritti da una direzione e un verso) o non orientati (di verso arbitrario).  
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
Il k-esimo tratto che congiunge i nodi \\(i\\) e \\(j\\) viene scritto come \\(e_k = (v_i, v_j)\\).

La _teoria dei grafi_ vede la luce per la prima volta nel 1736, grazie a __Eulero__. Il matematico svizzero, infatti, risolse il problema dei _sette ponti di Königsberg_ utilizzando quella che sarebbe poi diventata la teoria dei grafi. Eulero si chiedeva se fosse possibile partire e arrivare nello stesso punto della città attraversando tutti i ponti una sola volta.  
Grazie alle basi poste da Eulero, la teoria dei grafi si è evoluta ed è tutt'ora impiegata nella descrizione e nella risoluzione di _reti di acquedotti_ o in algoritmi per il calcolo del percorso (chiuso) più breve tra tutte le città del mondo (più info sulla soluzione potete trovarle [qui](http://www.math.uwaterloo.ca/tsp/world/)).

La teoria dei grafi è - come ogni teoria matematica - descritta da teoremi che non esporrò, per non tediarvi con argomentazioni facilmente reperibili altrove.

<h3 style="text-transform:uppercase">Ma quindi?</h3>

Il titolo descrive alla perfezione ciò che è presente nelle righe che seguono: "è possibile rappresentare una matrice attraverso un grafo?"  
La risposta è "sì, si può!"  
E non solo: è anche possibile derivare una matrice da un grafo.

----------

<div style="font-family:serif; margin:auto; width:50%; text-align:left; text-transform:uppercase; color:rgb(110,110,110)">
<h3>
 "è possibile rappresentare una matrice attraverso un grafo?" <br/>
La risposta è "sì, si può!"</h3>
</div>

-----------
to be continued...