markovTextStego.js
==================

This is a text steganography library for JavaScript that is a port of Hernan Moraldo's [markovTextStego](https://github.com/hmoraldo/markovTextStego).

Installation
------------

    <script src="markovTextStego.js"></script>
    
Usage
-----

Initial setup:

    var stego = new markovTextStego();
    
Create n-gram model:

    var model = new stego.NGramModel(n);
    
    // Import corpus (an array of messages, lines, paragraphs, etc.):
    model.import(corpus);
    
Initialise the Codec:

    var codec = new stego.Codec(model);
    
Encode &amp; Decode:

    codec.encode('Hello World!');
    codec.decode('The Achaeans. And with a moderate force of which one has to remark that men ought either to the kingdom! In exchange for the priesthood? Were San Pietro ad Vincula. He was obliged to avoid one trouble without running into another but prudence consists in knowing how lukewarm he was priest and that those men who were besieging Gaeta. In charge of Messer Antonio the priest to the shoulders of the counsellors will think of himself.');

Special Thanks
--------------
* Hernan Moraldo ([@hmoraldo](https://github.com/hmoraldo/))
* Umair Idris ([@umairidris](https://github.com/umairidris))
