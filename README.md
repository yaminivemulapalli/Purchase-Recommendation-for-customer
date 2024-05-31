# Purchase-Recommendation-for-customer

**Dataset link** :https://docs.google.com/spreadsheets/d/1MtY9EK8uxxk9lYll-J6RiqHCoJTd5B4e/edit?usp=sharing&ouid=106538803601840737448&rtpof=true&sd=true <br> 
**Dataset description:**<br>
This Online Retail II data set contains all the transactions occurring for a UK-based and registered, non-store online retail between 01/12/2009 and 09/12/2011.The company mainly sells unique all-occasion gift-ware. Many customers of the company are wholesalers.<br>

**Attribute Information:**<br>
InvoiceNo: Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.<br>
StockCode: Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.<br>
Description: Product (item) name. Nominal.<br>
Quantity: The quantities of each product (item) per transaction. Numeric.<br>
InvoiceDate: Invice date and time. Numeric. The day and time when a transaction was generated.<br>
UnitPrice: Unit price. Numeric. Product price per unit in sterling (Â£).<br>
CustomerID: Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.<br>
Country: Country name. Nominal. The name of the country where a customer resides.<br>

Source:
Dr. Daqing Chen, Course Director: MSc Data Science. chend '@' lsbu.ac.uk, School of Engineering, London South Bank University, London SE1 0AA, UK.<br>

**Aim**:Recommend the customers products based on their previous purchase history.<br>
Target variables:CustomerId,stockcode,description,quantity.<br>
Dependent variables: stockcode,description.<br>
Independent variables: CustomerId,Invoicedate,Quantity.<br>

**Data cleaning:**<br>
1)Remove the records whose price and quantity are negative values.<br>
2)Remove records whose customer ids are null.<br>
3)Remove the records whose Stockcode=POST -- indicating the online purchases of shipping charges,discounts.<br>

**Data Processing**<br>
1)Group by customerid and stockcode along with quantity sum.<br>
2)Create a pivottable.<br>

**Recommed the items**<br>
1)Recommend by grouping the stockcode and description which aggregates by Quantity sum and sorts the recommendations.<br>
2)Give the input of customerId.
