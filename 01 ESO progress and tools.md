<style>
    h2, h3, h4{
        color: Tomato;
    }
</style>
# Esmeraldo de Situ Orbis

- 1892 edition - printed . pdf 188 pag
- 1750 edition - handwritten . pdf 216 pag

## 1. Structure

### 2021 RUTTER Edition
<details><summary>[show/hide]</summary>
- `<front>`
- `<body>`
- `<back>`
</details>

### 1892 ed.
<details><summary>[show/hide]</summary>
- `<front>` <!-- TODO MM: verificar termos tags do <front> -->

  - [ ] cover
  - [ ] titlepage
  - [ ] titlepage 2
  - [ ] aknowledge
  - [ ] preliminar news
  - [ ] documents
  - [ ] table of contents
  - [ ] prologue

- `<body>`

  - [ ] first book . 33 chapters
  - [ ] second book . 1 intro + 11 chapters
  - [ ] third book . 1 intro + 9 chapters
  - [ ] fourth book . 1 intro + 6 chapters

- `<back>`

  - [ ] notes
  - [ ] personalities and geopgraphy index
  - [ ] index

</details>

#### Notes:

- PDF pag 163-164 in between printed pagination 106-107

<!-- TODO MM : create diferente file for: snippets | markdown | regex | TODO -->

#### Questions:
__1.__ 21-0928 MM: When reference of the same edition, is `<lb/>` placed before `<pb/>`?
- 21-0928 MM: Together the programmer might have more control over the code and content displayed.

__2.__ 21-0929 MM: ESO 1982 being a printed work belongs to `listBibl`, while ESO 1750, a manuscript, to `listWit`?
> Note also that if the witnesses being recorded are not manuscripts but printed works, it may be preferable to document them using the standard bibl or biblStruct elements
> [12.1.4.3 The Witness List](https://tei-c.org/release/doc/tei-p5-doc/en/html/TC.html#TCAPWL)

- 21-0929 MM : Is this right? If the work content is going to be used as variant, declare as `<witness>`. If the work or its content is as bibliographic reference, declare as `<bibl>` on `<listBibl>`. TEI by Examble does [this](https://teibyexample.org/tutorials/TBED07v00.htm?target=listWit#listWit): `<witness><bibl></bibl></witness>`.

- 21-0929 MM : To simplify. `<witness>` and `<bibl>`, are purpose or physical object driven tags?
