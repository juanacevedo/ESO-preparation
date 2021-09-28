## Esmeraldo Situ Orbis
### Tagging Guidelines

#### Index
* [TEI Header - Source Description](#the-source-description)

    1. [Source Description](#1-source-description)
    2. [List Objects](#2-list-objects)
    3. [List Organizations](#3-list-organizations)
    4. [List Persons](#4-list-persons)
    5. [List Persons](#5-list-places)
    6. [List Witnesses](#6-list-witnesses)

* [TEI Text](#tei-text)

    7. [Page beginning](#7-page-beginning)
    8. [Line beginning](#8-line-beginning)
    9. [Choices](#9-choices)
    10. [~~Numbers and Measures~~](#10-numbers-and-measures)
    <!-- TODO MM : numbers | date | notes | -->

<br/>

---
<br/>

#### The Source Description
<details><summary>[show/hide]</summary>
<br/>

##### 1. Source Description
tags : [`sourceDesc`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html)

Preferable organization of code as any list entry can be referenced from text encoding. Entries can be more detailed and packed in a single place than along the file. This keeps the code clean, reusable, accessable.

__Example:__
```xml
<sourceDesc>
    <listObject>
        <!-- list objects/animals --></listObject>
    <listOrg>
        <!-- list organizations --></listOrg>
    <listPerson>
        <!-- list persons --></listPerson>
    <listPlace>
        <!-- list places --></listPlace>
    <listWit>
        <!-- list witness: Ed. 1750, 1892 --></listWit>
</sourceDesc>
```
[&#x25b2; Return to Index](#index)

<br/>

##### 2. List Objects
tags : [`listObject`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listObject.html)  [`object`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-object.html)

__Example:__ [`object` examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-object.html)
```xml
<listObject>
    <object xml:id="EXC">
        <objectIdentifier>
            <objectName type="main">Excalibur</objectName>
            <country>Wales</country>
            <idno type="carter">256a</idno>
        </objectIdentifier>
        <msContents></msContents>
        <physDesc></physDesc>
    </object>
    <object></object>
</listObject>

<!-- [...] -->

<p>The famous <objectName ref="#EXC">Excalibur</objectName> was lost.</p>
```
[&#x25b2; Return to Index](#index)

<br/>

##### 3. List Organizations
tags : [`listOrg`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listOrg.html) [`org`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-org.html)

Contains a list of elements, each of which provides information about an identifiable organization.

__Example:__ [`org` examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-org.html)
```xml
<listOrg>
    <org xml:id="WC3">
        <orgName>World Wide Web Consortium</orgName>
        <desc>Founded in 1994 and currently led by Tim Berners-Lee, the consortium is made up of member organizations that maintain full-time staff working together in the development of standards for the World Wide Web.</desc>
    </org>
    <org></org>
</listOrg>

<!-- [...] -->

<p>The <orgName ref="#W3C" type="org">WC3</orgName> was lost.</p>
```
[&#x25b2; Return to Index](#index)

<br/>

##### 4. List Persons
tags : [`listPerson`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPerson.html) [`person`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-person.html)

Contains a list of descriptions, each of which provides information about an identifiable person or a group of people, for example the participants in a language interaction, or the people referred to in a historical source.

__Example:__ [`person` examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-person.html)
```xml
<listPerson>
    <person xml:id="jdoe">
        <persName>
            <forename></forename>
            <surname></surname>
        </persName>
        <birth></birth>
        <death></death>
        <nationality></nationality>
        <occupation notBefore="" notAfter=""></occupation>
        <occupation from="" to=""></occupation>
    </person>
    <person></person>
</listPerson>

<!-- [...] -->

<p><persName ref="#jdoe">John</persName> lived in Lyon and ...</p>
```
[&#x25b2; Return to Index](#index)

<br/>

##### 5. List Places
tags : [`listPlace`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPlace.html) [`place`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-place.html)

Contains a list of places, optionally followed by a list of relationships (other than containment) defined amongst them.

__Example:__ [`place` examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-place.html)
```xml
<listPlace>
    <place xml:id="lyon">
        <geogName>Mount Sinai</geoName>
        <placeName xml:lang="" notBefore="1400">Lyon</placeName>
        <placeName xml:lang="" notAfter="0640">Lugdunum</placeName>
        <location>
            <address></address>
            <bloc>EU</bloc>
            <country>France</country>
            <geo>45.769559 4.834843</geo>
        </location>
        <idno type=""></idno>
    </place>
    <place></place>
</listPlace>

<!-- [...] -->

<p>He lived in <placeName ref="#lyon">Lyon</placeName> and ...</p>
```
[&#x25b2; Return to Index](#index)

<br/>

##### 6. List Witnesses
tags : [`listWit`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listWit.html) [`witness`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-witness.html)

Lists definitions for all the witnesses referred to by a critical apparatus, optionally grouped hierarchically.

__Example:__ [`witness` examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-witness.html)
```xml
<encodingDesc>
    <variantEncoding method="parallel-segmentation" location="internal"/>
</encodingDesc>

<!-- [...] -->

<listWit>
    <witness xml:id="ESO-1892"></witness>
    <witness xml:id="ESO-1750"></witness>
</listWit>

<!-- [...] -->
<!-- TODO MM : verify lem wit="" value -->
<app>
    <lem wit="">word or expression</lem>
    <rdg wit="#ESO-1892">word / expression</rdg>
    <rdg wit="#ESO-1892">expression / word</rdg>
</app>
```
<br/>

__Note 2:__ No whitespaces are to be kept around the `<lb>` tag, as the programmer codes that decision depending on the purpose: text with fix-width or dynamic, or a toggle option.
[&#x25b2; Return to Index](#index)
</details>
<br/>

---

#### 2. TEI Text
<details><summary>[show/hide]</summary>

##### 7. Page beginning
tags : [`pb`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-pb.html)

Marks the beginning of a new page in a paginated document.

__Example:__ [`pb` examples](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/examples-pb.html)
```xml
<listBibl>
    <bibl xml:id="ESO-1892"></bibl>
    <bibl xml:id="ESO-1892"></bibl>
</listBibl>

<!-- [...] -->
<!-- TODO MM : can edRef point to witness ? -->

<p>There is more than
    <pb edRef="#EOS-1892"/>one page
    <pb edRef="#EOS-1750"/>around here.</p>
```

[&#x25b2; Return to Index](#index)

<br/>

##### 8. Line beginning
tags : [`lb`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-lb.html)

Marks the beginning of a new typographic line in some edition or version of a text. Some times it breaks a word, a hyphen comes in place, but some books might not always print the hyphen.

__Example:__
```xml
<p>The quick
    <lb/>brown fox jumps o
    <lb break="no"/>ver the la
    <lb break="no" type="hyphenated">zy dog</p>

```
<br/>

__Note 1:__ The use `type="hyphenated"` allows a programmer to control wherever show the hyphen or not, in case of wanting to be precise about an edition. Idea stolen from [The Newton Project](https://www.newtonproject.ox.ac.uk/about-us/tagging-and-transcription-guidelines).

__Note 2:__ No whitespaces are to be kept around the `<lb>` tag, as the programmer codes that decision depending on the purpose: text with fix-width or dynamic, or a toggle option.

[&#x25b2; Return to Index](#index)

<br/>

##### 9. Choices
tags : [`choice`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-choice.html) [`abbr`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-abbr.html) [`corr`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-corr.html) [`expan`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-expan.html) [`orig`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-orig.html) [`reg`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-reg.html) [`sic`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-sic.html) [`unclear`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-unclear.html)

Groups a number of alternative encodings for the same point in a text.

__Note 1:__ The `app` element is in one sense a more sophisticated and complex version of the `choice` element introduced [...] as a way of marking points where the encoding of a passage in a single source may be carried out in more than one way. Unlike `choice`, however, the `app` element allows for the representation of many different versions of the same passage taken from different sources. - [12.1 Apparatus Entry](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPLL)

__Note 2:__ Because the children of a `choice` element all represent alternative ways of encoding the same sequence, it is natural to think of them as mutually exclusive. However, there may be cases where a full representation of a text requires the alternative encodings to be considered as parallel. - [`choice` Note](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-choice.html)

<br/>

__Example:__ [`choice` examples](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/examples-choice.html)
```xml
<choice>
    <orig>favour</orig>
    <reg>favor</reg>
</choice>

<choice>
    <corr>dates</corr>
    <sic>date's</sic>
</choice>

<choice>
    <abbr>RELAX NG</abbr>
    <expan>regular language for
        <choice>
            <abbr>XML</abbr>
            <expan>extensible markup language</expan>
        </choice>, next generation
    </expan>
</choice>
```

[&#x25b2; Return to Index](#index)

<br/>

##### 10. Numbers and Measures







</details>
