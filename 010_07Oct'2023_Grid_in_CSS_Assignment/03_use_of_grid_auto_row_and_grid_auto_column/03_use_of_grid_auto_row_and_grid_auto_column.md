"grid-auto-rows" and "grid-auto-columns" properties are used to specify the size of implicitly generated rows and columns within a grid. For example in the code below:

 .container{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            grid-auto-flow: column;
            grid-auto-columns: 250px;
 }

 we have explicitely defined two grid columns to take 1 fr size each and 2 grid rows to take 1 fr each and grid auto flow is set to column. so when we add more than 4 grid items in the container then new item will create a new column and as that column size is not explicitely set in grid template , so it will be decided by grid-auto-column property which in this example sets the new column width to 250px.

 Similarily in the example code below:

  .container{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            grid-template-rows: repeat(2, 1fr);
            grid-auto-rows: 250px;
        }

in this example code above if we add a 5th item or more items in the grid container they will create  new rows as by default grid-auto-flow is set to row. and this new row will have a height of 250 px as defined by grid -auto-rows property.