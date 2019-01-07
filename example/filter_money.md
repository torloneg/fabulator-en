
Currency conversion functions are based on data in configuration and represent the conversion rate 

Example of currency conversion :

### TEMPLATE
```
* Money in GBP **{{data.accounting.money_1}}** converted into **{{ data.accounting.money_1| Money.Convert("GBP","USD") | Accounting.NumberFormat(2, ".", ",")}}** american dollars.

* The last price of BASF shares is **{{data.accounting.money_5}} Euro** (**{{ data.accounting.money_5| Money.Convert("EUR","USD") | Accounting.NumberFormat(2, ".", ",")}} {{ "USD" | Money.Symbol() }})**

* The dollar closed on the world's major currencies at **{{ 1| Money.Convert("USD","EUR") | Accounting.NumberFormat(2, ".", ",")}} {{ "EUR" | Money.Symbol() }}**, Japanese yen **{{ 1| Money.Convert("USD","JPY") }} {{ "JPY" | Money.Symbol() }}**, Turkish lira  **{{ 1| Money.Convert("USD","TRY") | Accounting.NumberFormat(2, ".", ",")}} {{ "TRY" | Money.Symbol() }}**, British pound **{{ 1| Money.Convert("USD","GBP") }} {{ "GBP" | Money.Symbol() }}**


* IT: l'{{ "EUR" | Money.SymbolExt("it",false,true) }} oggi vale **{{ 1| Money.Convert("EUR","USD") | Accounting.NumberFormat(2, ".", ",")}} 
{{ "USD" | Money.SymbolExt("it",true,true) }}**
* EN: the {{ "EUR" | Money.SymbolExt("en",false,false) }} today is **{{ 1| Money.Convert("EUR","USD") | Accounting.NumberFormat(2, ".", ",")}} {{ "USD" | Money.SymbolExt("en",true,true) }}**
```


### RESULT
* Money in GBP 12345678 converted into 16.135.820,99 american dollars.

* The last price of BASF shares is 0.615 Euro (0,72 $)

* The dollar closed on the world's major currencies at 0,86 €, Japanese yen 112.055 ¥, Turkish lira 6,17 ₺, British pound 0.76511 £

* IT: l'euro oggi vale 1,16 dollari americani

* EN: the euro today is 1,16 american dollars



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
	 
	 
	 
	 
