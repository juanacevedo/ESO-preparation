### Schema Guidelines

### Index
* [ODD - One Document Does it all](#odd---one-document-does-it-all)  

    1. [Schemma Speficication](#1-schema-specification)
    
<br/>

---
<br/>

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
