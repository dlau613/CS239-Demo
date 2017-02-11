Download free 14 Day Trial Here
https://www.tableau.com/products/desktop/download

Download Example Dataset
https://www.tableau.com/sites/default/files/getting_started_data_sets.zip

Connect to a File
Select Excel under Connect > To a File and select ‘Global Superstore Orders 2016.xlsx’

There are two sheets in the excel file, Orders and People. Drag orders to where it says ‘Drag sheets here’.

Add another connection. This time select Text file and select ‘Global Superstore Returns 2016.csv’.

![alt text](images/1AddConnection.png)

 It automatically adds the sheet and does a default cross database join. Click on the join symbol to see its details. To see all the information in Orders and the return information for transactions that were returned, select a Left Join. Leave Order ID as the join clause.

![alt text](images/2LeftJoin.png)

Manipulating the Fields
Click on the dropdown menu of the Order ID column and select Custom Split.
Type ‘-’ as the separator and select OK. We can see a new column is added. Go to its dropdown menu and rename it to Distribution Center

Now that we’ve set up our data source, select the Sheet 1 tab near the bottom left corner.

Visualization
Let’s analyze the sales per Category, Customer Segment, and Market based on the number of items sold.
Drag Category and Segment to Rows, and Quantity and Market to Columns. Also drag Market to Color.

The result should look like:
![alt text](images/3MarketSales.png)

Drilling Down
First clear the sheet by selecting the shortcut in the tool bar.
Drag Sales to Rows and Order Date to Columns. We now see sales increase over the four years there is data for. 
Click the ‘+’ symbol next to YEAR(Order Date) to drill down to the Quarters in each year. Flip Quarter and Year to view the data in quarters over years instead.
Drag Years to Color to see all the lines for each year on the same graph.
We can easily change the scope at which data is aggregated. Select the drop down menu for Quarters and select Month.
We can also change the measure of Sales. It is currently SUM but we could change it to another measure such as average or median.

Year over Year Growth
Select Quick Table Calculation>Year Over Year Growth in the drop down menu for Sales.

Add Sales to Rows and move the Year over Year Growth one to Tooltip. Now when we hover over the lines we can see the Year over Year Growth information.

We see a consistent dip in sales in July. By right clicking the graph, and selecting Annotate>Point we can leave an annotation on the graph. This image could easily be shared by right clicking the graph and selecting Copy>Image.

To see the data behind the graph, we can select Copy>Data and paste it into Excel. Or, right click the sheet tab in the lower right corner and select Duplicate as Crosstab

Swap the rows and columns so we can see our data better.
To visualize how profits are drag Profit to Color. If the colors make it difficult to interpret, click Color and select Edit Colors. You can change the color scheme and check Stepped Color. Also, change the Mark Type to Square and turn on Mark Labels.

![alt text](images/4ProfitsColors.png)

Add Category to Rows. Then under Category’s drop down menu select Show Highlighter. Using the highlighter we can easily differentiate between the different categories. We see that Furniture does not have as good of profits near the end of the year.

Let’s create a new sheet to investigate this further.



