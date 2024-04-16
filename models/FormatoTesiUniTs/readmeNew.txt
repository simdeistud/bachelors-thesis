Il Latex:
---------

Per scrivere la tesi si raccomanda l’uso di Latex 2e. Una breve guida del Latex 2e può essere reperita a questo indirizzo http://ctan.mirror.garr.it/mirrors/CTAN/info/lshort/italian/itlshort.pdf.
Latex è un sistema per la produzione di documenti che segue la stessa logica dei linguaggi di programmazione. Di conseguenza, il primo passo da compiere nella stesura della tesi è quello di preparare alcuni sorgenti latex (per i vari capitoli, le eventuali appendici e la bibliografia), che dovranno poi essere compilati per produrre la tesi in formato dvi, successivamente convertibile in formato postscript (visualizzabile attraverso ghostview) oppure pdf (visualizzabile attraverso acrobat reader).
I file del direttorio forniscono già un template per scrivere la tesi.

La seguente guida illustra i passi necessari all'installazione dei 
pacchetti necessari per poter utilizzare il template di tesi presente.

Ambiente Linux:
---------------
Le istruzioni si riferiscono all'installazione di Texmaker su una
distribuzione GNU/Linux di tipo Red Hat-like.

Installazione:
- Aprire una finestra di terminale come utente amministratore (root);
- Installare Texmaker e i pacchetti necessari per una compilazione
 mediante il seguente comando:
	yum install texmaker texlive-babel-italian texlive-hyphen-italian texlive-subfigmat texlive-appendix
 Le dipendenze verranno installate automaticamente all'esecuzione 
 del comando. Qualora si volesse ricompilare l'esempio installare anche il pacchetto texlive-lipsum.

Procedura di compilazione
- Aprire il file Tesi.tex con Texmaker;
- Compilare Tesi.tex con PDFLaTeX;
- Compilare Tesi.tex con BibTeX;
- Compilare Tesi.tex con PDFLaTeX per due volte.

Ambiente Windows:
-----------------
Sotto Windows si può utilizzare l’ambiente di sviluppo integrato freeware TeXstudio (http://texstudio.sourceforge.net/) oppure TeXnicCenter (http://www.texniccenter.org/). A tale scopo, si consiglia di installare (in quest’ordine) il compilatore miktex (http://www.miktex.org/), l’interprete del linguaggio postscript ghostscript (http://www.ghostscript.com/), l’applicazione ghostview (http://pages.cs.wisc.edu/~ghost/gsview/index.htm) ed infine l’ambiente TeXstudio oppure TeXnicCenter. Per compilare la tesi è sufficiente compilare più volte il file Tesi.tex.

Per garantire la fattibilità del copia-incolla dal file pdf da consegnare, si consiglia di utilizzare la sequenza di comandi di compilazione latex --> dvips --> ps2pdf oppure latex --> dvipdfm oppure semplicemente pdflatex (consigliato per il template allegato). Inoltre, le vocali accentate vanno inserite nei sorgenti con gli appositi comandi latex “\`a“, “\`e“, “\'e“, “\`{\i}“, “\`o“, “\`u” e non con i tasti delle vocali accentate stesse. E’ possibile usare le lettere accentate da tastiera solo se i file latex sono salvati nel formato UTF8 e viene incluso il package “inputenc” con l’opzione utf8 (con \usepackage[utf8]{inputenc}). 

I font:
-------

La tesi in PDF deve fare solo uso di font type 1. Tale verifica può essere fatta in Acrobat, mediante File->Proprietà->Fonts.  L’header del file tesi.tex (negli esempi) impone già l’uso solo di font Type 1, ma qualora tali font non siano tutti installati nella propria macchina ne verranno usati anche altri (es. Type 3). Qualora nella tesi siano usati font diversi dal Type 1, va installato il package cm-super e va ricompilata la tesi. Sotto Linux, il package può essere installato come qualunque altro pacchetto. Sotto Windows, usando Miktex, può essere installato con il package manager (Tutti i Programmi -> Miktex -> maintinance (Admin) -> Package Manager): basta cercare cm-super e cliccando con il tasto destro richiedere install (il pacchetto è installato solo quando il campo “Installed On” riporta una data).

Il contenuto dei file:
----------------------

I contenuti veri e propri della tesi sono contenuti nei file 
contenuti nelle directory:
- front: contiene la parte iniziale della tesi (copertina, sommario, 
  dedica iniziale, introduzione);
- main: contiene i capitoli principali della tesi;
- back: contiene le conclusioni, le appendici e la dedica finale;
- bib: contiene il file Bibliografia.bib da ripempire secondo la sintassi
  di BibTeX.

Organizzazione della tesi:
--------------------------

La tesi deve essere organizzata in capitoli e deve riportare alla sua fine l’indicazione di tutte le fonti bibliografiche dalle quali si sono attinte informazioni. Di norma il primo capitolo della tesi introduce il contesto nel quale si colloca il lavoro, il problema affrontato in quel contesto, l’idea che sta alla base della soluzione proposta ed infine l’indicazione di come è strutturato il resto della tesi. Analogamente, l’ultimo capitolo della tesi di norma riepiloga il lavoro svolto e fornisce prospettive di possibili sviluppi futuri. Il numero di pagine consigliato è compreso tra 30 e 50