## Esmeraldo Situ Orbis
### Tagging Guidelines

__Note__ This is a \"work in progress\" draft of an first approach to the guidelines to be used of this project, hence the introductory tone and examples.
A more torward definitive tag composition is placed after the code examples, as being worked for improvement.

#### Index
* [TEI Header - Source Description](#the-source-description)

    1. [Source Description](#1-source-description)
    2. [List Objects](#2-list-objects)
    3. [List Organizations](#3-list-organizations)
    4. [List Persons](#4-list-persons)
    5. [List Places](#5-list-places)
    6. [List Witnesses](#6-list-witnesses)
    7. [~~List Animalia~~](#7-list-animalia)
    8. [~~List Plantae~~](#8-list-animalia)

* [TEI Text](#tei-text)

    1. [Page beginning](#1-page-beginning)
    2. [Line beginning](#2-line-beginning)
    3. [Choices](#3-choices)
    4. [~~Numbers and Measures~~](#4-numbers-and-measures)
    5. [~~Dates~~](#5-dates)
    6. [~~Notes~~](#6-notes)
    7. [~~Geographic Location~~](#7-geographic-location)
    8. [Critical Apparatus](#8-critical-apparatus)

* [ODD - One Document Does it all](#odd---one-document-does-it-all)  

    1. [Schemma Speficication](#1-schema-specification)

<br/>

---
<br/>

### The Source Description

[TEI Guidelines - 2.2.7 The Source Description](https://tei-c.org/release/doc/tei-p5-doc/en/html/HD.html#HD3)
> The sourceDesc element is the seventh and final component of the fileDesc element. It is a mandatory element and is used to record details of the source or sources from which a computer file is derived. This might be a printed text or manuscript, another computer file, an audio or video recording of some kind, or a combination of these.

<details open><summary>[show/hide]</summary>
<br/>

#### 1. Source Description
tags : [`sourceDesc`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html)

Preferable organization of code as any list entry can be referenced from text encoding. Entries can be more detailed and packed in a single place than along the file. This keeps the code clean, reusable, accessable.

__Example:__
```xml
<sourceDesc>
    <!-- TODO MM : How to point animalia references? -->
    <listBibl>
        <!-- list bibliographic references --></listBibl>
    <listObject>
        <!-- list objects --></listObject>
    <listOrg>
        <!-- list organizations --></listOrg>
    <listPerson>
        <!-- list persons --></listPerson>
    <listPlace>
        <!-- list places --></listPlace>
    <listWit>
        <!-- list witness --></listWit>
</sourceDesc>
```

<br/>

__Proposed (WIP)__
```xml
<!-- TODO MM : confirm other contents: listBibl, etc -->
<sourceDesc>
    <listBibl></listBibl>
    <listObject></listObject>
    <listOrg></listOrg>
    <listPerson></listPerson>
    <listPlace></listPlace>
    <listWit></listWit>
</sourceDesc>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 2. List Objects
tags : [`listObject`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listObject.html)  [`object`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-object.html)

__Example:__ [`object`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-object.html)
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

<br/>

__Proposed (WIP)__
```xml
<listObject>
    <object xml:id="">
        <!-- TODO MM : object inner tags -->
    </object>
</listObject>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 3. List Organizations
tags : [`listOrg`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listOrg.html) [`org`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-org.html)

Contains a list of elements, each of which provides information about an identifiable organization.

__Example:__ [`org`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-org.html)
```xml
<listOrg>
    <org xml:id="WC3">
        <orgName>World Wide Web Consortium</orgName>
        <desc>Founded in 1994 and currently led by Tim Berners-Lee, the consortium is made up of member organizations that maintain full-time staff working together in the development of standards for the World Wide Web.</desc>
    </org>
    <org></org>
</listOrg>

<!-- [...] -->

<p>The <orgName ref="#W3C" type="org">WC3</orgName> has a nice website.</p>
```

<br/>

__Proposed (WIP)__
```xml
<listOrg>
    <org xml:id="">
        <!-- TODO MM : org inner tags -->
    </org>
</listOrg>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 4. List Persons
tags : [`listPerson`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPerson.html) [`person`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-person.html)

Contains a list of descriptions, each of which provides information about an identifiable person or a group of people, for example the participants in a language interaction, or the people referred to in a historical source.

__Example:__ [`person`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-person.html)
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

<br/>

__Proposed (WIP)__
```xml
<!-- TODO MM : person inner tags -->
<listPerson>
    <person xml:id="">
        <!-- NAMES --> <!-- mandatory -->
        <persName xml:lang="">
            <forename></forename>
            <surname></surname>
        </persName>
        <!-- BIRTH --> <!-- mandatory -->
        <birth when="" notAfter="" notBefore="">
            <placeName ref="">
                <country ref=""></country>
                <region ref=""></region>
                <settlement ref=""></settlement>
            </placeName>
        </birth>
        <!-- DEATH --> <!-- mandatory -->
        <death when="" notAfter="" notBefore="">
            <placeName ref="">
                <country ref=""></country>
                <region ref=""></region>
                <settlement ref=""></settlement>
            </placeName>
        </death>
        <sex></sex>
        <idno></idno>
        <nationality></nationality>
        <occupation type="" from="" to=""></occupation>
        <residence></residence>
        <note>
            <p></p>
        </note>
    </person>
</listPerson>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 5. List Places
tags : [`listPlace`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPlace.html) [`place`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-place.html)

Contains a list of places, optionally followed by a list of relationships (other than containment) defined amongst them.

__Example:__ [`place`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-place.html)
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

<br/>

__Proposed (WIP)__
```xml
<listPlace>
    <!-- Place -->
    <place xml:id="">
        <!-- TODO MM : place oriented inner tags -->
    </place>

    <!-- Geographic -->
    <place xml:id="">
        <!-- TODO MM : geographic oriented inner tags -->
    </place>
</listPlace>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 6. List Witnesses
tags : [`listWit`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listWit.html) [`witness`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-witness.html)

Lists definitions for all the witnesses referred to by a critical apparatus, optionally grouped hierarchically.

__Example:__ [`witness`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-witness.html)
```xml
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

__Proposed (WIP)__
```xml
<!-- TODO MM : study tag: variantEncoding -->
<encodingDesc>
    <variantEncoding method="parallel-segmentation" location="internal"/>
</encodingDesc>

<!-- [...] -->

<listWit>
    <witness xml:id="">
        <!-- TODO MM : witness inner tags -->
    </witness>
</listWit>
```
<br/>

[&#x25b2; Return to Index](#index)
</details>

<br/>

#### 7. List Animalia
tags : [` `]()

Yet to define proper method.
<!-- TODO MM : animalia yet to define proper method -->

__Examples:__
```xml
```

<br/>

__Proposed (WIP)__
```xml
```

[&#x25b2; Return to Index](#index)

<br/>

#### 8. List Plantae
tags : [` `]()

Yet to define proper method.
<!-- TODO MM : plantae yet to define proper method -->

__Examples:__
```xml
```

<br/>

__Proposed (WIP)__
```xml
```

[&#x25b2; Return to Index](#index)

<br/>

---

### TEI Text
<details open><summary>[show/hide]</summary>

#### 1. Page beginning
tags : [`pb`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-pb.html)

Marks the beginning of a new page in a paginated document.

__Example:__ [`pb`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/examples-pb.html)
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

<!-- <pb/> @n="page number" facs="link_page_image" -->
<p>A page ends here.
    <pb edRef="#EOS-1750" n="8" facs="https://purl.pt/27102/1/1897597_JPG/1897597_JPG_24-C-R0150/1897597_0008_t24-C-R0150.jpg">just to start around the corner.</p>
```

<br/>

__Proposed (WIP)__
```xml
    <!-- LV1 priority -->
    <pb edRef=""/>

    <!-- LV2 priority : if possible / workload -->
    <pb edRef="" n="" facs="">
```
[&#x25b2; Return to Index](#index)

<br/>

#### 2. Line beginning
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

<br/>

__Proposed (WIP)__
```xml
<p>
    <lb edRef=""/>
    <lb edRef="" break="no"/>
    <lb edRef="" break="no" type="hyphenated">
</p>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 3. Choices
tags : [`choice`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-choice.html) [`abbr`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-abbr.html) [`corr`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-corr.html) [`expan`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-expan.html) [`orig`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-orig.html) [`reg`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-reg.html) [`sic`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-sic.html) [`unclear`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-unclear.html)

Groups a number of alternative encodings for the same point in a text.

__Note 1:__ The `app` element is in one sense a more sophisticated and complex version of the `choice` element introduced [...] as a way of marking points where the encoding of a passage in a single source may be carried out in more than one way. Unlike `choice`, however, the `app` element allows for the representation of many different versions of the same passage taken from different sources. - [12.1 Apparatus Entry](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPLL)

__Note 2:__ Because the children of a `choice` element all represent alternative ways of encoding the same sequence, it is natural to think of them as mutually exclusive. However, there may be cases where a full representation of a text requires the alternative encodings to be considered as parallel. - [`choice` Note](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-choice.html)

<br/>

__Example:__ [`choice`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/examples-choice.html)
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

<br/>

__Proposed (WIP)__
```xml
```

[&#x25b2; Return to Index](#index)

<br/>

#### 4. Numbers and Measures
<!-- TODO MM : numbers and measures content -->
tags :
```xml
```

<br/>

__Proposed (WIP)__
```xml
```
[&#x25b2; Return to Index](#index)

<br/>

#### 5. Dates
<!-- TODO MM : dates content -->
tags :
```xml
```

<br/>

__Proposed (WIP)__
```xml
```
[&#x25b2; Return to Index](#index)

<br/>

#### 6. Notes
<!-- TODO MM : notes content -->
tags :

[note on app example](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-app.html#index-egXML-d39e91097)
```xml
```

<br/>

__Proposed (WIP)__
```xml
```
[&#x25b2; Return to Index](#index)

<br/>

#### 7. Geographic Location
<!-- TODO MM : improve content -->
tags : [`geoDecl`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-geoDecl.html) [`location`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-location.html) [`geo`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-geo.html)

__Examples:__ [`location`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-location.html) [`geo`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-geo.html)
```xml
<encodingDesc>
    <geoDecl xml:id="WGS" datum="WGS84">World Geodetic System</geoDecl>
    <geoDecl xml:id="OS" datum="OSGB36">Ordnance Survey</geoDecl>
</encodingDesc>

<!-- [...] -->

<!-- pontual reference -->
<location>
    <geo decls="#WGS">53.226658 -0.541254</geo>
</location>
```

<br/>

__Proposed (WIP)__
```xml
<encodingDesc>
    <geoDecl xml:id="">
        <!-- TODO MM : deoDecl inner tags -->
    </geoDecl>
</encodingDesc>
```
[&#x25b2; Return to Index](#index)

<br/>

#### 8. Critical Apparatus
tags : [`app`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-app.html) [`lem`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-lem.html) [`rdg`](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-rdg.html)

TEI Chapter [12. Critical Apparatus](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html)

__Variant Encoding__ methods:
- [`location-referenced`](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPLO): low precision, and prevents the reconstration of the lemma for each variant.
- [`double-end-point`](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPDE): just as precise as parallel-segmentation, it differs in the ability to manage \"overlapping lemmata\". Here is an [example](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#index-egXML-d52e100519).
- [`parallel-segmentation`](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPPS): \"This method differs from the double end-point attachment method in that all variants at any point of the text are expressed as variants on one another. In this method, no two variations can overlap, although they may nest.\"  
\"This method will (by definition) always be satisfactory when there are just two texts for comparison (assuming they are in the same language and script). It will however be less convenient for textual traditions where establishing a base text with variations from it is not a satisfactory goal for the edition, or in some cases where every detail of variation needs to be modeled.\"  

__Examples:__ [`app`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-app.html) [`lem`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-lem.html) [`rdg`](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-rdg.html)
```xml
<encodingDesc>
    <variantEncoding method="parallel-segmentation" location="internal"/>
</encodingDesc>

<!-- [...] -->

<app>
    <lem wit="#El #Hg">Experience</lem>
    <rdg wit="#La" type="substantive">Experiment</rdg>
    <rdg wit="#Ra2" type="substantive">Eryment</rdg>
</app>
```

__Proposed (WIP)__
```xml
<!-- If <lem> is an editorial normalization (is it the same as conjecture?),
     @resp takes the editorial person @id -->
<app xml:id="" type="">
    <lem resp="" cause=""></lem>
    <rdg wit="" type=""></rdg>
    <rdg wit="" type=""></rdg>
</app>


<!-- Being <lem> value the content of the RUTEER ESO printed edition,
     does @wit points to itself in a <bibl> or <witness> entry? TODO -->
<app xml:id="" type="">
    <lem wit=""></lem>
    <rdg wit="" type=""></rdg>
    <rdg wit="" type=""></rdg>
</app>
```

[&#x25b2; Return to Index](#index)

<br/>

</details>

### ODD - One Document Does it all

<details open><summary>[show/hide]</summary>
<br/>

#### 1. Schema Speficication
[TEI by Examble - Module 8: Customising TEI, ODD, Roma](https://teibyexample.org/tutorials/TBED08v00.htm)  
[TEI Guidelines - 22.8 Building a TEI Schema](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/TD.html#TDbuild)  



tags : [`schemaSpec`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-schemaSpec.html) [`moduleRef`](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-moduleRef.html)  
attributes:  
[att.identified](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-att.identified.html): `@ident` `@predeclare` `@module`  
[att.combinable](https://www.tei-c.org/release/doc/tei-p5-doc/en/html/ref-att.combinable.html): `@mode`

__Examples:__
```xml
<!-- link schemas to our TEI file -->
<?xml-model href="tei_tite.rng" type="application/xml" ?>
<?xml-model href="checkLinks.sch" type="application/xml" schematypens="http://purl.oclc.org/dsdl/schematron" ?>
<?xml-model href="tei_tite.odd" type="application/tei+xml" schematypens="http://www.tei-c.org/ns/1.0" ?>

<!-- [...] -->

<!-- ODD schemaSpec element -->
<schemaSpec ident="T​BEcustom" start="T​EI" prefix="tei_" targetLang="en" docLang="en">
    <!-- required minimal header elements -->
    <moduleRef key="header" include="tei​Header file​Desc title​Stmt publication​Stmt source​Desc"/>
    <!-- required core elements (p and title for use in titleStmt) -->
    <moduleRef key="core" include="p title"/>
    <!-- required textstructure elements (TEI, text, and body) -->
    <moduleRef key="textstructure" include="T​EI text body"/>
    <!-- required module tei instantiates lots of classes used for further expansion of this odd -->
    <moduleRef key="tei"/>

    <!-- or directly specify the elements to be included, without need to specify its module -->
    <elementRef key="linkGroup"/>
    <!-- or directly specify subset of attributes -->
    <classRef key="att.global.linking" include="corresp"/>
</schemaSpec>
```

<br/>

__Proposed (WIP)__
```xml
<schemaSpec ident="TEIP5_ESO_custom" docLang="pt">
    <moduleRef key="header"
        include=""/>
    <moduleRef key="core"
        include=""/>
    <moduleRef key="textstructure"
        include=""/>
    <moduleRef key="tei"/>
</schemaSpec>
```


<!-- ######################################## TOPIC Template:

#### 14. Critical Apparatus
tags : [``]()

__Examples:__
```xml
```

<br/>

__Proposed (WIP)__
```xml
```

[&#x25b2; Return to Index](#index)

<br/>

-->
