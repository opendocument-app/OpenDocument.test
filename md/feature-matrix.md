# Feature matrix

The decoder's own fixture: one block or span per row of the mapping table in
`src/odr/internal/markdown/AGENTS.md`, so the reference output pins what each
one renders to.

## Headings

### Third level

#### Fourth level

##### Fifth level

###### Sixth level

## Paragraphs and inline marks

A paragraph with a soft break
that is a space, and a hard break  
that is a line break.

*Emphasis*, **strong**, ***both nested***, ~~struck through~~ and `inline
code`. Entities: &amp; &lt; &gt; &quot; &#65; &#x42; &nbsp; and &notanentity;
stays literal.

A [link](https://opendocument.app/) and an ![image](nowhere.svg) whose alt text
is all that is modelled.

## Lists

- a tight item
- another, whose text needs an implicit paragraph for its marker
  - nested one level
- back out again

* a loose list

* whose items are paragraphs already

3. an ordered list counting from three
4. and on

1) the other delimiter

- [ ] an open task
- [x] a done one

## Block quotes

> One level, whose paragraphs carry a left margin.
>
> > Two levels, carrying twice as much.

## Code

```cpp
int main() {
  return 0;  // two spaces of indent survive as &nbsp;
}
```

    an indented code block
      with a deeper line

## Table

| left | centre | right |
|:-----|:------:|------:|
| a    | b      | c     |
| 1    | 2      | 3     |

## Nothing in the model

A horizontal rule renders as nothing:

---

<div>and a raw html block is dropped entirely</div>

Inline <b>html</b> is dropped too, though its text survives.
