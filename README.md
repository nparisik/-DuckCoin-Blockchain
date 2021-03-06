# Educoin
Educoin is a cryptocurrency to be used by students of Stevens Institute of Technology. 
The client can control the blockchain involved in the Educoin and also the price of Educoin. 
Users can transfer money from one user account to another, 
and they can also exchange other forms of currency for Educoins.

## Getting Started
### Prerequisites
* [Python 3.6](https://www.python.org/downloads/) - IDLE included
	* [Flask] Flask Module for python
	* [Requests] Requests Module for python
	* [RSA] RSA Module for python
* [Postman](https://www.getpostman.com/apps) - for blockchain/transaction management

### Configuration
```
After installing the programs listed above, open "blockchain.py" in IDLE and run it.
This message should be displayed if these steps have been followed correctly:
```
![python_works](/docs/python_works.png)


```
Open Postman, a greeting message will appear. Select "Create a basic request" as shown:
```
![postman_intro](/docs/postman_intro.png)

```
Enter "blockchain" as the request, and (optionally) a description. Create/select a folder to save the request to.
Your Postman window should look like this:
```
![postman_basic](/docs/postman_basic.png)

### Using Postman
When using Postman in conjunction with our "blockchain.py" file, there are a few key items
to pay attention to:
![postman_watch](/docs/postman_watch.png)

```
The dropdown menu with "GET" allows different commands for sending/receiving data.
Use GET if you're requesting to view the blockchain, resolve node conflicts,
etc. Use POST when you'd like to create a transaction, register a new node, etc.
```

```
The address bar can be found to the right of the dropdown mentioned above. Enter the address
of the node that will be making requests.
```

```
The SEND button to the right of the address bar is used to send requests. Press it after
entering the address of the node and any other details needed.
```

```
The "Body" tab under the address bar allows for any necessary information to be added.
For example, extra information is needed when creating a transaction, such as amount 
and users. 
```

```
The dropdown menu containing "Text", "HTML", and "JSON" must have JSON selected for 
our requests to function properly.
```
### Postman Commands
There are a few different actions we can take using Postman at this step.
NOTE: change the address in each of the commands below with the address of the node
being used. To make life easier you can import all of the following reqeusts by importing the Postman folder into the Postman application. This will create a collection and environment that you can use to simplify typing in the entire request everytime. They will serve as templates so feel free to modify them. Also make sure that you set your environment in postman correctly to use these templates with variables. 
For the purpose of following these instructions, the address below is fine.

* Mine a block
```
GET request to "http://localhost:5000/mine"
```

* Create a transaction
```
POST request to "http://localhost:5000/transactions/new" with a body containing
our transaction structure, which can be seen below
```
![postman_transactions](/docs/postman_transactions.png)


* View the full blockchain
```
GET request to "http://localhost:5000/chain"
```

* Registering new nodes - allows for a user to connect to the network
```
POST request to "http://localhost:5000/register"
```

* Resolve potential node conflicts
```
GET request to "http://localhost:5000/resolve"
```

### Postman Examples
```
Here is an example of mining a block using Postman:
```
![postman_mine](/docs/postman_mine.png)

## Built With
* [Python 3.6](https://www.python.org/downloads/)
* [Hackernoon](https://hackernoon.com/learn-blockchains-by-building-one-117428612f46)
* [Postman](https://www.getpostman.com/apps)

## Authors
* Nick Parisik
* Aviksith Pilly
* Josh Pirog
* Nicholas Polich
* Ben Rose
* Lauren Sachs

## License 
This project is licensed under the MIT license -- see the LICENSE.md file for details.

## Acknowledgements
* Daniel van Flymen of Hackernoon for his exceptional code
* Dr. Dimitrios Damopoulos for his inspiration towards the project
