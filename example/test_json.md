# JSON TEST

The examples refer to a json with various types of data.

```
{
	"string": "Feature",
	"string_1": "this is a string",
	"person": {
		"first_name": "jhon",
		"last_name": "smith",
		"sex": "M"
	},
	"person_m": {
		"first_name": "jhon",
		"last_name": "smith",
		"sex": "M"
	},
	"person_f": {
		"first_name": "rose",
		"last_name": "smith",
		"sex": "F"
	},
	"time": "2014-09-08T04:49:20Z",
	"string_true_1": "1",
	"string_true_2": "true",
	"string_false_1": "0",
	"string_false_2": "false",
	"string_int": "1",
	"string_float": "1.1",
	"date2year": "2014-01-01T04:49:20Z",
	"accounting": {
		"money_1": 12345678,
		"money_2": -500000,
		"money_3": 4999.99,
		"money_4": 5318008,
		"money_5": 0.615
	},
	"units": {
		"unit_less_1": 0.543,
		"unit_1": 1,
		"unit_more_1": 1.232,
		"unit_more_100": 123.093,
		"unit_more_1000": 1630.093
	},
	"number": 3,
	"number_0": 0,
	"number_1": 1,
	"number_2": 2,
	"sign": {
		"positive": 1,
		"negative": -1,
		"parity": 0
	},
	"double": 2.1,
	"array_1": [
		1,
		1,
		1,
		1,
		1,
		1
	],
	"array_1_0": [
		1,
		1,
		1,
		1,
		1,
		0
	],
	"array_0": [
		0,
		0,
		0,
		0,
		0,
		0
	],
	"array_0_1": [
		0,
		0,
		0,
		0,
		0,
		1
	],
	"array_2": [
		2,
		2,
		2,
		2,
		2
	],
	"array_number": [
		1,
		2,
		3,
		4,
		5,
		6,
		7,
		8,
		9,
		10
	],
	"array": [
		"first",
		"second",
		"third",
		"fourth",
		"fifth"
	],
	"geometry": {
		"type": "Point",
		"coordinates": {
			"latitude": 13.3157262,
			"longitude": 42.3633634,
			"deep": 7000.65
		}
	},
	"collection": [
		{
			"item_id": "1092",
			"description": "ELEMENT #1",
			"date": "2017-08-09"
		},
		{
			"item_id": "2192",
			"description": "ELEMENT #2",
			"date": "2017-07-08"
		},
		{
			"item_id": "2193",
			"description": "ELEMENT #3",
			"date": "2018-07-08"
		}
	],
	"string_comma": "first, second, third, fourth, fifth",
	"http": {
		"host": "http://localhost:3001/api/reader/mongodb/v1/findone/",
		"dictonary": "ecommerce_item",
		"key": 2191
	}
}

```