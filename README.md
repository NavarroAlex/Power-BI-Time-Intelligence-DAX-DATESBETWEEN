# Time Intelligence DAX: DATESBETWEEN

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Power%20BI%20Theme.png)

## Author
[alex.navarro@danone.com]

## Link to Microsoft DAX Documentation:
[https://learn.microsoft.com/en-us/dax/datesbetween-function-dax]

## DATESBETWEEN DAX Definition:
Returns a table that contains a column of dates that begins with a specified start date and continues until a specified end date.

## Syntax:
```
DATESBETWEEN(<Dates>, <StartDate>, <EndDate>)
```

## Parameters:
![ScreenShot](https://github.com/NavarroAlex/Time-Intelligence-DAX-DATESBETWEEN/blob/main/Parameter%20Values.png)

## Demonstration:
* Dataset to use is the "300. Order to Cash Dataset"
* Columns to use:
    - Gross Sales
    - Bill Date

DAX Code:
```
Mid Season Sales = 
-- calculate
CALCULATE(
    -- sum total sales: round two decimal places:
    ROUND(SUM('`Order to Cash'[Gross Sales]),2),
    -- input dates between:
    DATESBETWEEN('Bill Date'[Bill Date],
    DATE(2022, 10, 01),
    DATE(2022, 10, 18)
    )
)
```

## Final Example Output:
![ScreenShot](https://github.com/NavarroAlex/Time-Intelligence-DAX-DATESBETWEEN/blob/5666bff6d2e27706de3409fc0454e995d9cd28db/Final%20Example.png)

