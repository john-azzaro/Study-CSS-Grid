# CSS Grid Study 

## What is the CSS Grid Study?
CSS Grid study is a practical examination of CSS Grid, a two dimensional layout system which allows you to control positioning, sizing, and spacing of content.  Anything declared in the grid will adapt to the columns and rows defined.

<br>

## What are the key terms we need to know?
* **Grid CONTAINERS**
   * The grid container establishes how the grid will be formatted.
   * It also manages how all the child elements are spaced, sized, and aligned.
   * For uniformity, use the ".grid" class. 
   
* **Grid ITEMS**
   * Everything inside the grid container are the grid container's children
   
* **Grid LINES**
   * Lines between the grid items (within the gird container).
   * Grid column lines start from left to right from 1 to X.
   * Grid row lines starts from top to bottom from 1 to X.
   * A grid line is not a complete column or row, they only outline the row or the column.
      * For example, column 1 would have 2 grid lines on the left and right side.
      * As another example, a three column layout would have 4 gird lines.

   Example:
   ```
    <main class="grid">            \\ *main is the parent container* \\
        <section>...</section>     \\ sections are the child items \\
        <section>...</section>
        <section>...</section>
    </main>
   ```

* SUMMARY: The grid CONTAINER (".grid") contains all the child ITEMS within it.  The grid template COLUMNS and gird template ROWS provide us with numbered grid LINES that we use for positioning the items.


<br>

## Positioning and Aligning Content to the Grid

* The grid is formed by intersecting sets of hrozontal and veritcal lines call **grid lines**.
* Grid lines divide the contianer space into **columns and rows**, or areas in which items are aligned and placed.
* **Horizontal grid lines** position **rows**.
* **Veritical grid lines** position **columns**. 

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