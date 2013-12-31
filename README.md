markovTextStego.js
==================

This is a text steganography library for JavaScript adapted from [Hernan Moraldo](http://www.hernan.moraldo.com.ar/)'s [reference implementation](https://github.com/hmoraldo/markovTextStego) for &ldquo;[An Approach for Text Steganography Based on Markov Chains](http://www.41jaiio.org.ar/sites/default/files/3_WSegI_2012.pdf)&rdquo;. This method produces more natural looking and less easily detectable texts than other Markov-based systems.

In this implementation, n-gram models support updating and n values of &ge; 1.

An online interactive demo is available [**here**](http://jthuraisamy.github.io/markovTextStego.js/).

Installation
------------

    <script src="markovTextStego.js"></script>

Usage
-----

Initial setup:

    var stego = new MarkovTextStego();

Create n-gram model:

    var model = new stego.NGramModel(n);

    // Import corpus (an array of strings: messages, lines, paragraphs, etc.)
    model.import(corpus);

Initialise the Codec:

    var codec = new stego.Codec(model);

Encode &amp; Decode:

    codec.encode('Hello World!');
    codec.decode('The Achaeans. And with a moderate force of which one has to remark that men ought either to the kingdom! In exchange for the priesthood? Were San Pietro ad Vincula. He was obliged to avoid one trouble without running into another but prudence consists in knowing how lukewarm he was priest and that those men who were besieging Gaeta. In charge of Messer Antonio the priest to the shoulders of the counsellors will think of himself.');

Update the model with an array of additional corpus text:

    model.update(additionalCorpus);

Change the model to a different one:

    codec.setModel(newModel);

Limitations
-----------

* Corpus must contain at least two unique sentences/lines with each consisting of two or more words.

Acknowledgements
----------------
* Hernan Moraldo ([@hmoraldo](https://github.com/hmoraldo/))
* Umair Idris ([@umairidris](https://github.com/umairidris))

Licence
-------

[MIT](http://www.tldrlegal.com/l/MIT)
