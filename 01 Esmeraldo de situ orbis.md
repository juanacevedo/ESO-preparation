# Esmeraldo de Situ Orbis

* 1892 edition - printed . pdf 188 pag
* 1750 edition - handwritten . pdf 216 pag

## 1. Structure

### 1892 ed.

- front <!-- TODO MM: verificar termos tags do <front> -->
    - [ ] cover
    - [ ] titlepage
    - [ ] titlepage 2
    - [ ] aknowledge
    - [ ] preliminar news
    - [ ] documents
    - [ ] table of contents
    - [ ] prologue
- body
    - [ ] first book . 33 chapters
    - [ ] second book . 1 intro +  11 chapters
    - [ ] third book . 1 intro + 9 chapters
    - [ ] fourth book . 1 intro + 6 chapters
- back
    - [ ] notes
    - [ ] personalities and geopgraphy index
    - [ ] index

###### Notes:
* PDF pag 163-164 in between printed pagination 106-107

### 1750 ed.

## 2. TEI - project guidelines

* Page break / Line break for different editions
```xml
<pb n="001" edRef="#idEdition"/>
<lb n="001" edRef="#idEdition"/>
```


## 3. TEI - Examples
* tag witness
```xml
<witness xml:id="p2">
    <bibl>
        <editor>Sperberg​-McQueen, M.</editor>;
        <editor>Burnard, L.</editor> (eds.).
        <title>T​EI P2 Guidelines for the Encoding and Interchange of Machine Readable Texts Draft P2</title>
        (published serially 1992​-1993); Draft Version
        <date when="1993​-04​-02">2 of April 1993</date>:
        <extent>19 chapters</extent>.
        Available from
        <ptr target="https​://tei​-c.org​/Vault​/Vault​-GL.html"/>
        (accessed October 2008).
    </bibl>
</witness>
```
