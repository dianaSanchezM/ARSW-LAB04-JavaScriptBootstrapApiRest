# FrontEnd - JavaScript Base Client
# URL HEROKU: https://arswlab4apirestbootstrap.herokuapp.com/

Create a simple front end using the following frameworks:
 - [bootstrap](https://getbootstrap.com)
 - [axios](https://github.com/axios/axios)
 - [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)

# Part 1: Create a basic html page using a Bootstrap template

  1. Go to the boostrap examples and download the code and extract the following template:
  https://getbootstrap.com/docs/4.0/examples/cover/
  
  2. Update your html code to have the following menu items:
  - orders
  - new order
  
 3. Update the  content of your page (where the learn more button is located) with a table that will display the order with hardcoded values:
  
**Order 1:**


  | Product | Quantity | Price | 
  | ------------- | ----- |:-------------:| 
  |PIZZA|3|$10000| 
  |HOTDOG|1|$3000|
  |COKE|4|$1300|

# Part 2: Implement the FrontEnd controller

1. Create a JavaScript file called  **OrdersController.js**
2. Create a JavaScript object list that represents the table on Part 1 on the Order **OrdersController.js** (Do not forget to add an id attribute to the Order object).

```javascript
{
	"order_id": 1,
	"table_id": 1,
	"products": [{
			"product": "PIZZA",
			"quantity": 3,
			"price": "$15.000"
		},
		{
			"product": "HAMBURGER",
			"quantity": 1,
			"price": "$12.300"
		}
	]
}
```

3. Create a function that adds an order (a new table below the existing Order 1 table).
4. Create a function that removes an order table with a given id: *removeOrderById(int id)*
    Use the following method to start: https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById
5. Try your add order function iterating the list created on 2. and make sure the data is loaded into the table from the JavaScript code.

6. Create a function that loads the orders (creates the HTML tables) from a mocked list of orders in your JavaScript file.
Once this function is working call it from the body tag in order to invoke this function everytime the page is loaded:

```html
	<body onload="loadOrders();">
```

# Part 3: Consume the REST API and connect it with the FrontEnd
1. Create a function that calls the API Endpoint that retrieves the orders list using the [Axios API library](https://github.com/axios/axios)
2. Implement the callback when the orders list is return succesfully that uses the *OrderController.js* functions.
3. Modify the loadOrders function so it actually makes a call to the Orders API and loads the orders from the server.
4. Implement the callback when the request fails that shows a dialog to user saying that "There is a problem with our servers. We apologize for the inconvince, please try again later" 
5. In order to test your application do the following:
    - Add your JavaScript file to the SpringBoot project under the resources/static/js folder (create the folder if it does not exist)
    - Add your html page (index.html) to the resources/static folder
6. Create a Heroku project and deploy your SpringBoot then test that it works as expected.
