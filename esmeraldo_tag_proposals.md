## Esmeraldo Situ Orbis
### Tagging Guidelines

#### Index
1. [The Source Description](#the-source-descriptions)
    1. [sourceDesc]()
    2. [listObject]()
    3. [listOrg]()
    4. [listPerson]()
    5. [listPlace]()
    6. [listWit](#listwit)
2. Page break

<br/>

---
<br/>

#### The Source Description
<br/>

##### 1. sourceDesc
tags : [sourceDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html)

Preferable organization of code as any list entry can be referenced from text encoding. Entries can be more detailed and packed in a single place than along the file, and without chance of reference.

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
    <br/>

    2. __listObject__
    <br/>[listObject](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listObject.html) . [object](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-object.html)

    __Example:__ [object examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-object.html)
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

    3. __listOrg__
    <br/>[listOrg](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listOrg.html) . [org](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-org.html)

    Contains a list of elements, each of which provides information about an identifiable organization.

    __Example:__ [org examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-org.html)
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
    <br/>

    4. __listPerson__
    <br/>[listPerson](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPerson.html) . [person](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-person.html)

    Contains a list of descriptions, each of which provides information about an identifiable person or a group of people, for example the participants in a language interaction, or the people referred to in a historical source.

    __Example:__ [person examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-person.html)
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

    5. __listPlace__
    <br/>[listPlace](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listPlace.html) . [place](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-place.html)

    Contains a list of places, optionally followed by a list of relationships (other than containment) defined amongst them.

    __Example:__ [place examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-place.html)
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

    6. __listWit__
    <br/>[listWit](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listWit.html) . [witness](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-witness.html)

    Lists definitions for all the witnesses referred to by a critical apparatus, optionally grouped hierarchically.

    __Example:__ [witness examples](https://tei-c.org/release/doc/tei-p5-doc/en/html/examples-witness.html)
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
        <lem wit="">word or wxpression</lem>
        <rdg wit="#ESO-1892">word / expression</rdg>
        <rdg wit="#ESO-1892">expression / word</rdg>
    </app>
    ```
