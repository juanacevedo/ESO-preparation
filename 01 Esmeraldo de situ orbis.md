# Esmeraldo de Situ Orbis

* 1892 edition
* 1750 edition

## 1. Structure

- &lt;front&gt; <!-- TODO MM: verificar termos tags do <front> -->
    - [ ] cover
    - [ ] titlepage
    - [ ] titlepage 2
    - [ ] aknowledge
    - [ ] preliminar news
    - [ ] documents
    - [ ] table of contents
    - [ ] prologue
- &lt;body&gt;
    - [ ] first book . 33 chapters
    - [ ] second book . 1 intro +  11 chapters
    - [ ] third book . 1 intro + 9 chapters
    - [ ] fourth book . 1 intro + 6 chapters
- &lt;back&gt;
    - [ ] notes
    - [ ] personalities and geopgraphy index
    - [ ] index


###### Notes:
* PDF pag 163-164 in between printed pagination 106-107

## 2. tags instances

Page Breaks for different editions
'''xml
<pb n="001" edRef="#idEdition"/>
'''

# Line break for diferent editions
'''xml
<lb n="001" edRef="#idEdition"/>
'''

# List of witness
##IF creating or generating a critical edition
'''xml
<sourceDesc>
    <listWit></listWit>
</sourceDesc>
'''

##IF digitising an existing critical edition
'''xml
<text>
    <front>
        <listWit></listWit>
    </front>
</text>
'''

```xml
<TEI xmlns="http://www.tei-c.org/ns/1.0">
    <teiHeader>
        <!-- mandatory -->
        <fileDesc>
            <!-- mandatory -->
            <titleStmt>
                <title></title>
                <author></author>
                <editor></editor>
                <sponsor></sponsor>
                <funder></funder>
                <principal></principal>
                <respStmt></respStmt>
            </titleStmt>
            <editionStmt>
                <edition></edition>
            </editionStmt>
            <extent>
                <!-- digital size -->
            </extent>
            <!-- mandatory -->
            <publicationStmt></publicationStmt>
            <seriesStmt></seriesStmt>
            <notesStmt></notesStmt>
            <!-- mandatory -->
            <sourceStmt></sourceStmt>
        </fileDesc>
        <encodingDesc></encodingDesc>
        <profileDesc></profileDesc>
        <revisionDesc></revisionDesc>
    </teiHeader>
    <text>
        <front>
            <titlepage></titlepage>
        </front>
        <body></body>
        <back></back>
    </text>
</TEI>
```
