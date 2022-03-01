# Turkish Wordnet
This repository contains the Turkish Wordnet that is built between 2001-2004 as part of the BalkaNet Project. 
It consists of three files:

- An XML file for the actual wordnet
- .def and .cfg files to visualise the wordnet with the Visdic tool.


To visualise and/or edit Turkish Wordnet, you can download Visdic from the following page:

http://nlp.fi.muni.cz/projekty/visdic/

In Visdic, open the XML file from  Files > Dictionaries and follow Visdic documentation for further actions.


## The XML Structure of Turkish Wordnet

The XML file consists of a series of `<SYNSET>` tags, each containing a single 
synset and its links to other semantically related synsets.

The `<ID>` tag is the unique synset identifier that links Turkish Wordnet to all
other wordnets built upon Princeton WordNet. The identifier ENG20-07172978-n,
for example, indicates that this synset was taken from Princeton Wordnet 2.0, has
the Princeton Wordnet 2.0 ID 07172978, and is a noun. Similarly, the identifier
BILI-60000008 indicates that this synset is one of the Balkanet-specific con-
cepts jointly developed by the six members of the Balkanet Consortium, and has
the Balkanet Inter-Lingual Index (BILI) identifier 60000008.

The `<POS>` tag contains part-of-speech information, where ‘n’ denotes a noun,
‘v’ a verb and ‘a’ an adjective. 

The `<SYNONYM>` tag contains the synset members within `<LITERAL>` tags, and their automatically assigned sense numbers within `<SENSE>` tags. 

The `<ILR>` tag is used to link the synset to another synset, where the `<TYPE>` tag indicates the type of the semantic relation in question. 
  
The `<DEF>` tag contains a brief definition of the concept, either in English or Turkish, and finally, the `<BCS>` tag indicates whether the synset belongs to one of the three Base
Concept sets defined during the Balkanet project. 


A single synset containing the synonymous words bitki and nebat ‘plant’ is shown below:

 ```
<SYNSET>
	<ID>ENG171-00012420-n</ID>
	<POS>n</POS>
	<SYNONYM>
		<LITERAL>
			bitki
			<SENSE>1</SENSE>
		</LITERAL>
		<LITERAL>
			nebat
			<SENSE>1</SENSE>
		</LITERAL>
	</SYNONYM>
	<ILR>
		ENG171-00003135-n
		<TYPE>hypernym</TYPE>
	</ILR>
	<ILR>
		ENG15-06531331-n
		<TYPE>holo_member</TYPE>
	</ILR>
	<DEF>Bulunduğu yere kökleriyle tutunup gelişen, döl
	veren ve hayatını tamamladıktan sonra kuruyarak
	varlığı sona eren, yosun, ot, ağaç gibi canlıların
	genel adı.
	</DEF>
	<BCS>1</BCS>
</SYNSET>

```
  
## Publications

Çetinoğlu, Özlem, Orhan Bilgin, and Kemal Oflazer\
*Turkish Wordnet*\
In: ed. by Kemal Oflazer and Murat Saraçlar\
Theory and Applications of Natural Language Processing. Springer International Publishing\
Chap. 15, pp. 317–336.

```
@incollection{cetinoglu2018,
 title = {{Turkish} {Wordnet}},
  author={{\c{C}}etino{\u{g}}lu, {\"O}zlem
        and Bilgin, Orhan and Oflazer, Kemal},
 chapter = {15},
 pages = {317--336},
 year = {2018},
 booktitle={Turkish Natural Language Processing},
  editor={Oflazer, Kemal and Sara{\c{c}}lar, Murat},
  isbn={9783319901657},
  series={Theory and Applications of Natural Language Processing},
  publisher={Springer International Publishing}
}
```
  
Bilgin, Orhan, Özlem Çetinoğlu, and Kemal Oflazer\
*Building a WordNet for Turkish*\
In: Romanian Journal of Information Science and Technology\
7.1-2, pp. 163–172

```
@article{bilgin2004,
  title={Building a {WordNet} for {Turkish}},
  author={Bilgin, Orhan and {\c{C}}etino{\u{g}}lu, {\"O}zlem and Oflazer, Kemal},
  journal={Romanian Journal of Information Science and Technology},
  volume={7},
  number={1-2},
  pages={163--172},
  year={2004},
  publisher={Romanian Academy}
}
```
