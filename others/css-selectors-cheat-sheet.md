# CSS Selectors Cheat Sheet

### **Cheat sheet of common selectors** <a href="#cheat-sheet-of-common-selectors" id="cheat-sheet-of-common-selectors"></a>

`head` selects the element with the `head` tag

`.red` selects all elements with the ‘red’ class

`#nav` selects the elements with the ‘nav’ Id

`div.row` selects all elements with the `div` tag and the ‘row’ class

`[class="true"]` selects all elements with the `class` attribute with a value of “true”

* \[name^="abc"]
* \[name$="abc"]
* \[name\*="abc"]

### We can combine selectors in interesting ways <a href="#we-can-combine-selectors-in-interesting-ways" id="we-can-combine-selectors-in-interesting-ways"></a>

#### Some examples: <a href="#some-examples" id="some-examples"></a>

`li a` DOM descendant combinator. All `a` tags that are a child of `li` tags

`div.row *` selects all elements that are descendant (or child) of the elements with `div` tag and ‘row’ class

`li > a` Difference combinator. Select direct descendants, instead of all descendants like the descendant selectors

`li + a` The adjacent combinator. It selects the element that is immediately preceded by the former element. In this case, only the first `a` after each `li`.

`li, a` Selects all `a` elements and all `li` elements.

`li ~ a` The sibling combinator. Selects `a` element following a `li` element.

### Pseudo-selectors or pseudo structural classes <a href="#pseudo-selectors-or-pseudo-structural-classes" id="pseudo-selectors-or-pseudo-structural-classes"></a>

These are also useful for selecting structural elements from the DOM.

#### Here are some of them: <a href="#here-are-some-of-them" id="here-are-some-of-them"></a>

`:first-child` Target the first element immediately inside (or child of) another element

`:last-child` Target the last element immediately inside (or child of) another element

`:nth-child()` Target the nth element immediately inside (or child of) another element. Admits integers, `even`, `odd`, or formulas

`a:not(.name)` Selects all `a` elements that are not of the `.name` class

`::after` Allows inserting content onto a page from CSS, instead of HTML. While the end result is not actually in the DOM, it appears on the page as if it is. This content loads after HTML elements.

`::before` Allows inserting content onto a page from CSS, instead of HTML. While the end result is not actually in the DOM, it appears on the page as if it is. This content loads before HTML elements.

We can use pseudo-classes to define a special state of an element of the DOM. But they don’t point to an element by themselves .

#### Some examples: <a href="#some-examples--1" id="some-examples--1"></a>

`:hover` selects an element that is being hovered by a mouse pointer

`:focus` selects an element receiving focus from the keyboard or programattially

`:active` selects an element being clicked by a mouse pointer

`:link` selects all links that have not been clicked yet

`:visited` selects a link that has already been clicked

### More info on the nth-child selector <a href="#more-info-on-the-nth-child-selector" id="more-info-on-the-nth-child-selector"></a>

The `nth-child` selector is a css psuedo-class taking a pattern by which to match one or more elements relative to their position among siblings.

#### Syntax <a href="#syntax" id="syntax"></a>

```css
  a:nth-child(pattern) {
    /* Css goes here */
  }
```

#### **Pattern** <a href="#pattern" id="pattern"></a>

The patterns accepted by `nth-child` can come in the form of keywords or an equation of the form An+B.

**Keywords**

**Odd**

Odd returns all odd elements of a given type.

```css
  a:nth-childe(odd) {
    /* CSS goes here */
  }
```

**Even**

Even returns all even elements of a given type.

```css
  a:nth-childe(even) {
    /* CSS goes here */
  }
```

**An+B**

Returns all elements matching the equation An+B for every positive integer value of n (in addition to 0).

For example, the following will match every 3rd anchor element:

```css
  a:nth-childe(3n) {
    /* CSS goes here */
  }
```
