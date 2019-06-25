---
title: "La Teoria dei Fili"
date: 2019-03-13T21:58:49+01:00
draft: false
tags: ["post"]
author: "anzo559"
---

L'elaborato che ho esposto [durante la mia laurea](/post/my-degree) tratta la **teoria dei fili** con elementi di storia e applicazione alle strutture civili.

In questa pagina descriverò brevemente i concetti contenuti nella tesi che potete visualizzare e scaricare gratuitamente a [questo link](https://osf.io/9zgdc/).

Il documento è stato redatto completamente in `LaTeX` e `TiKZ`. Il codice sorgente è disponibile in formato compresso al [seguente link](https://osf.io/prf76/).

Prima di iniziare devo ringraziare il **[Prof. Stefano Siboni](http://www.ing.unitn.it/~siboni/)** che è stato disponibile per ogni dubbio e chiarimento lungo tutto il periodo di stesura della tesi.

## La Fune
La fune è uno degli elementi costruttivi più utilizzato nella storia, almeno in campo civile.  
Nonostante i primi avvistamenti di fili di rame risalgano al 700 a.C., le prime applicazioni della fune avvengono durante il *XV* secolo con la comparsa dei primi **ponti inca** e dei famosi **ponti tibetani**.  
Nonostante lo stesso periodo storico in cui sono stati sviluppati, questi ponti sono radicalmente differenti. Mentre in sudamerica gli *inca* costruivano le funi intrecciando delle corde, in Tibet il fisico e ingegnere *Tangtong Gyalpo* utilizzò delle lunghe catene in ghisa per comporre la struttura portante di quello che sarebbe diventato il primo ponte tibetano.

{{<figure src="/images/Ponte_Inca.jpg" title="Uno dei pochi ponti inca sopravvissuti" width="100%">}}

A partire dalla rivoluzione industriale si ha un'evoluzione della fune, che diventa un elemento composito formato dalla posa, in diverse configurazioni, di fili di acciaio. Applicando queste nuove tecnologie alle strutture civili, in particolare ai ponti, si ottengono delle costruzioni snelle, leggere ed estremamente funzionali.

{{<figure src="/images/Ponte_Tibetano_Oggi.jpg" title="Ponte tibetano moderno" width="100%">}}


<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

<!--<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {
    inlineMath: [['$','$'], ['\\(','\\)']],
    displayMath: [['$$','$$'], ['\[','\]']],
    processEscapes: true,
    processEnvironments: true,
    skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
    TeX: { equationNumbers: { autoNumber: "AMS" },
         extensions: ["AMSmath.js", "AMSsymbols.js"] }
  }
});
</script>

<script type="text/x-mathjax-config">
  MathJax.Hub.Queue(function() {
    // Fix <code> tags after MathJax finishes running. This is a
    // hack to overcome a shortcoming of Markdown. Discussion at
    // https://github.com/mojombo/jekyll/issues/199
    var all = MathJax.Hub.getAllJax(), i;
    for(i = 0; i < all.length; i += 1) {
        all[i].SourceElement().parentNode.className += ' has-jax';
    }
});
</script>-->

## La Teoria dei Fili
<p>In <i>teoria dei fili</i> per fune si intende una curva regolare o biregolare di classe almeno <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML"><semantics><msup><mi>C</mi><mn>2</mn></msup><annotation encoding="application/x-tex">C^2</annotation></semantics></math> e di lunghezza assegnata.</p>

Per semplicità di calcolo, si ipotizza che la curva sia **inestensibile** e **perfettamente flessibile**. La prima condizione impone che non vi siano deformazioni lungo l'asse della fune, descritto dall'ascissa curvilinea `s`, il che equivale a porre la *rigidezza assiale* del filo **infinita**
$$EA\to\infty$$

La condizione di *perfetta flessibilità* si può descrivere come l'arbitrarietà del valore di curvatura della fune, implicando una rigidezza flessionale nulla
$$EI\to 0$$

Essendo il filo inestensibile e perfettamente flessibile, è facile capire che l'unica direzione delle forze esterne attive applicabili è quella parallela all'asse della fune e di verso uscente (**trazione**).

Dalle basi appena poste sulla teoria dei fili, applicando la meccanica classica a un tratto di filo finito soggetto a un sistema di forze distribuito, è possibile ottenere la **equazione indefinita di equilibrio** scritta in termini vettoriali come
$$ \frac{d\underline{T}}{ds}(s) + \underline{f}(s) = 0 $$
che risulta essere un sistema di 3 equazioni differenziali in 3 incognite (le 3 componenti di <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML"><semantics><munder><mi>T</mi><mo accent="false">̲</mo></munder><annotation encoding="application/x-tex">\underline{T}</annotation></semantics></math>).</p>

Applicando delle opportune *condizioni iniziali* si ottiene il **Problema di Cauchy** che ammette un'unica soluzione definita dal `teorema di esistenza e unicità della soluzione` applicato a un **dominio aperto**.

Discorso diverso è nel caso di imposizione delle condizioni al contorno. Per le condizioni al contorno, infatti, non esiste alcun teorema che assicuri l'esistenza e l'unicità della soluzione.  
E` comunque possibile risolvere il sistema di equazioni differenziali impiegando dei metodi numerici, non sapendo a priori se la soluzione effettivamente esista.

Il terzo e ultimo capitolo del documento riguarda l'applicazione della teoria dei fili a problemi in ambito civile. In particolare sono stati studiati i seguenti casi:

* equazione dei ponti sospesi;
* catenaria omogenea;
* filo soggetto a forze distribuite nulle;
* filo soggetto a forze concentrate.

Una volta ricavata l'equazione indefinita di equilibrio dalla teoria dei fili (**Capitolo 2**) è sufficiente applicarla ai differenti casi, ricavando soluzioni molto interessanti.

Consiglio al lettore, se interessato, di leggere l'elaborato e, nel caso avesse dubbi o volesse discutere di argomenti contenuti nell'elaborato, di scrivere un mail all'indirizzo  
**[matteo.franzoi-1@studenti.unitn.it](mailto:matteo.franzoi-1@studenti.unitn.it)**