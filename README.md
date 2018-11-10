# CSS Grid Study 

## What is the CSS Grid Study?
CSS Grid study is a practical examination of CSS Grid, a two dimensional layout system which allows you to control positioning, sizing, and spacing of content.  Anything declared in the grid will adapt to the columns and rows defined.

## What are the key terms we need to know?
* **Grid CONTAINERS**
   * The grid container esbalishes how the grid will be formatted.
   * It also manages how all the child elements are spaced, sized, and aligned.
   
<br>

* **Grid ITEMS**
   * Everything inside the grid container are the grid container's children
   
   Example:
   ```
    <main >                        (main is the parent container)
        <section>...</section>     (sections are the child items)
        <section>...</section>
        <section>...</section>
    </main>
   ```

<br>

## Positioning and Aligning Content to the Grid

* The grid is formed by intersecting sets of hrozontal and veritcal lines call **grid lines**.
* Grid lines divide the contianer space into **columns and rows**, or areas in which items are aligned and placed.
* **Horizontal grid lines** position **rows**.
* **Veritical gird lines** position **columns**. 

<br>

## Setting Up The Grid Container

In your HTML document, create a parent container and a few child grid items.
```
     <main class="">
        <section class="item">1</section>
        <section class="item">2</section>
        <section class="item">3</section>
    </main>
```