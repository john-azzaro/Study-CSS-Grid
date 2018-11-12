# CSS Grid Study 

## What is the CSS Grid Study?
CSS Grid study is a practical examination of CSS Grid, a two dimensional layout system which allows you to control positioning, sizing, and spacing of content.  Anything declared in the grid will adapt to the columns and rows defined.

<br>

## Basics of CSS Grid 

* **Grid CONTAINERS**
   * The grid container establishes how the grid will be formatted.
   * It also manages how all the child elements are spaced, sized, and aligned.
   * For uniformity, use the ".grid" class. 
   
* **Grid ITEMS**
   * Everything inside the grid container are the grid container's children
   
   Example:
   ```
    <main class="grid">                             \\ The main is the parent container
        <section class="childone">...</section>     \\ The three sections are the child items 
        <section class="childtwo">...</section>
        <section class="childthree">...</section>
    </main>
   ```

* **Grid LINES**
   * The grid is formed by intersecting sets of hrozontal and veritcal lines call **grid lines**.
   * Grid lines divide the contianer space into **columns and rows**, or areas in which items are aligned and placed.
   * **Horizontal grid lines** position **rows**.
   * **Veritical grid lines** position **columns**. 
   * Grid column lines start from left to right from 1 to X.
   * Grid row lines starts from top to bottom from 1 to X.
   * A grid line is not a complete column or row, they only outline the row or the column.
      * For example, column 1 would have 2 grid lines on the left and right side.
      * As another example, a three column layout would have 4 grid lines.

    Example:
    ```
        1           2           3           4
     1   ___________________________________         \\ First horizontal row grid line.
        | [column1] | [column2] | [column3] |        \\ 3 columns (tracks), 4 grid lines. 
     2   ___________________________________         \\ Second horizontal row grid line.                      
        | [column1] | [column1] | [column1] |        
     3   ___________________________________         \\ Third horizontal row grid line.
    ```


* SUMMARY: 
  The grid CONTAINER (".grid") contains all the child ITEMS within it.  The grid template COLUMNS and gird template ROWS provide us with numbered grid LINES that we use for positioning the items.

<br>

## Declarations to know

### minmax 

* This lets you set the grid track's minimum and maxium size.
* minimum size will let you make sure the content doesnt become to small or narrow where you cant see it.
* maximum size will let you make sure the content doesnt become to wide or tall.
* using minmax will help you build layouts that adapt to a wide range of screen sizes.

* to use minmax, use it in the ``` grid-template-columns ``` declaration.
```
grid-template-columns: minmax() 1fr 1fr;   // 3 tracks, first is a minmax, second and third are set to 1fr.
```
* minmax accepts two values, a minimum (first) and a maximum (last).  
* the value for min needs to be smaller than the value for maximum (otherwise browser will ignore the max value).
```
grid-template-columns: minmax(300px, 1fr) 1fr 1fr; ; 
```
* In the example above, there are three tracks.  the first track has a minmax function where the column will collapse no smaller than 300px.  The max is 1fr, maeing it will exand as needed.

...
...
...

<br>

## CSS Grid Boilerplate

### Basic CSS Grid HTML
```
    <main class="grid">
        <section class="item1">1</section>
        <section class="item2">2</section>
        <section class="item3">3</section>
        <section class="item4">4</section>
        <section class="item5">5</section>
    </main>
```
### Basic CSS Grid CSS Rulesets
```
* {
    box-sizing: border-box;                 /* Make sure sizing repsects the dimensions explicitly stated */                  
    margin: 0;                              /* Reset Rule: sets all elements to 0 margin. Helpful for making consistent designs.*/
    padding: 0;                             /* Reset Rule: sets all elements to 0 padding. Helpful for making consistent designs.*/                                                      
}


.grid {
    display: grid;                                                                             /* Display property type*/   
    grid-template-columns: minmax(150px, 1fr) minmax(50%, 1fr) minmax(150px, 1fr);             /* Column widths with minmax setting smallest and largest scales */
    grid-template-rows: minmax(50px, 100px) minmax(300px, 1fr) minmax(50px, 100px);            /* Row height with minmax setting shortest to tallest scales */
    height: 100vh;                                                                               
    grid-column-gap: 0;                                     
    grid-row-gap: 0;   
    grid-template-areas:
    "item1 item1 item1"
    "item2 item3 item4"   
    "item5 item5 item5"
    ;                     
}

        .item1 {
            grid-area: item1;
            background-color: lightblue;
        }

        .item2 {
            grid-area: item2;
            background-color: lightpink;   
        }

        .item3 {
            grid-area: item3;
            background-color: lightcyan;
        }

        .item4 {
            grid-area: item4;
            background-color: lightslategrey;   
        }

        .item5 {
            grid-area: item5;
            background-color: lightyellow;
        }
```













## Setting Up The Grid Container

In your HTML document, create a parent container and a few child grid items.
```
     <main class="">
        <section class="item">1</section>
        <section class="item">2</section>
        <section class="item">3</section>
    </main>
```