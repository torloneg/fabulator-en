## ACCOUNTING

Examples of accounting filter for number, money and currency formatting

## TEMPLATE
```
* a number **{{data.accounting.money_1}}** became "*the cash flow is* {{data.accounting.money_1 | Accounting.MoneyFormat}}" 
* a number **{{data.accounting.money_2}}** became "*the amount of the debt is {{data.accounting.money_2 | Accounting.MoneyFormat("$ ", 2)}}*"
* a number **{{data.accounting.money_3}}** became "*value of the investment is {{data.accounting.money_3 | Accounting.MoneyFormat("€ ", 2, ".", ",")}}*"
 
```

## RESULT
* a number 12345678 became "the cash flow is €12.345.678,00"
* a number -500000 became "the amount of the debt is $ -500.000,00"
* a number 4999.99 became "value of the investment is € 4.999,99"


####FORMAT
Accounting function can take a list of numbers and money-format them with padding to line up currency symbols and decimal places. 

## TEMPLATE
```
A list of number **[123.5, 3456.49, 777888.99, 12345678, -5432]** became **{{[123.5, 3456.49, 777888.99, 12345678, -5432] | Accounting.FormatColumn("€ ")}}**.

You can convert simple numbers by adding spaces to hundreds with custom accuracy :
**9876543.2123** became **{{9876543.2123 | Accounting.MoneyFormat("€ ", 2, " ")}}**
```

## RESULT
	 
A list of number **[123.5, 3456.49, 777888.99, 12345678, -5432]** became **€ 123.50,€ 3,456.49,€ 777,888.99,€ 12,345,678.00,€ -5,432.00**.

You can convert simple numbers by adding spaces to hundreds with custom accuracy : **9876543.2123** became **€ 9 876 543,21**

####NUMBER

## TEMPLATE
```
convert **{{data.accounting.money_1}}** to **{{data.accounting.money_1 | Accounting.NumberFormat}}** 

convert **{{data.accounting.money_2}}** to **{{data.accounting.money_2 | Accounting.NumberFormat(3, " ")}}**

convert **{{data.accounting.money_3}}** to **{{data.accounting.money_3 | Accounting.NumberFormat(2, ".", ",")}}** 
```


## RESULT
convert **12345678** to **12.345.678,00**

convert **-500000** to **-500 000,000**

convert **4999.99** to **4.999,99**


####FIX

## TEMPLATE
```
default precision is 2 and the number **{{data.accounting.money_5}}** became to **{{data.accounting.money_5 | Accounting.Fix}}**. If precision is 3 the number **{{data.accounting.money_5}}** is **{{ data.accounting.money_5| Accounting.Fix(3)}}**
```
## RESULT
default precision is 2 and the numerb **0.615** became to **0.62**. If precision is **3** the number **0.615** is **0.615**

  

###JSON snippet
   ```
    "accounting": {
	    "money_1":12345678,
	    "money_2":-500000,
	    "money_3":4999.99,
	    "money_4":5318008,
	    "money_5":0.615
	    
	}
     
```


	 
	 
