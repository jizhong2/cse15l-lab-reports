# Lab Report 2
<br> *Part 1*
<br> Below are screenshots of the code to ChatServer 
<br> ![Image](webserverpt1.png)
<br> ![Image](webserverpt2.png)

<br> Below are two ```/add-message``` on the webserver.
<br> ![Image](webservermsgs.png)
<br> Methods, handleRequest(), equals(), getQuery(), and split() was called on.
<br> The relevant argument was ```URI url``` for ```handleRequest()``` and relevant fields are ```String queryString```, ```String[] parameters```, ```String user```, and ```String message```.
<br> ```String queryString``` is dependent on ```URI url```, and ```String[] parameters```, ```String user```, ```String message``` depend on ```String queryString```. Once the method ```equals()``` checks and finds ```/add-message``` from the ```URI url```, it changes the values to ```String[] parameters```, ```String user```, ```String message``` depending on the values obtained from ```split()```, which changes the printed messages on the webserver. In this case, getQuery() got the value of ```String user``` "jpolitz" and the value of ```String message``` "Hello", and it printed "jpolitz: Hello".

<br> Edited:
<br> The relevant fields of the Handler class are ```String user```, ```String message```. These values will change once ```/add-messages?s=Hello&user=jpolitz``` is put into the URL. The ```split()``` will look for "&", "=", and "=" and ```contains()``` will search if "/add-message", "user", "s" are present. Once those are found, those values will be stored in their respective fields, such as ```String user``` and ```String message```. In this case, ```String user = "jpolitz"``` and ```String message = "Hello"```. With different values within the ```/add-message``` request, there will be different values stored/shown on the webserver.


<br> ![Image](webserver.png)
<br> Methods, handleRequest(), equals(), getQuery(), and split() was called on.
<br> The relevant argument was ```URI url``` and relevant fields are ```String queryString```, ```String[] parameters```, ```String user```, and ```String message```.
<br> ```String queryString``` is dependent on ```URI url```, and ```String[] parameters```, ```String user```, ```String message``` depend on ```String queryString```. 
<br> The method ```equals()``` checks and finds ```/add-message``` from the ```URI url```, ```String[] parameters```, ```String user```, ```String message``` depend on the values obtained from ```split()```, which changes the printed messages on the webserver. In this case, getQuery() got the value of ```String user``` "yash" and the value of ```String message``` "How are you", which printed "yash: How+are+you".

<br> Edited:
<br> The relevant fields of the Handler class are ```String user```, ```String message```. These values will change once ```/add-messages?s=How are you&user=yash``` is put into the URL. The ```split()``` will look for "&", "=", and "=" and ```contains()``` will search if "/add-message", "user", "s" are present. Once those are found, those values will be stored in their respective fields, such as ```String user``` and ```String message```. In this case, ```String user = "yash"``` and ```String message = "How+are+you"```.

<br> *Part 2*
<br>Below is the absolute path to the private key.
<br> ![Image](privatekey.png)
<br>
<br> Below is the absolute path to the public key.
<br> ![Image](publickey.png)
<br>
<br> Below is the terminal interaction.
<br> ![Image](terminal.png)
<br>

*Part 3*
<br> One thing I've learned throughout weeks 2 and 3 was how a URL has different parts. I learned with ```https://```, the ```s``` stands for secure and the domain is after ```https;//``` and ends with .org, .com, .edu, etc. How after ```/``` and before ```?``` is a path and after ```?``` is a query. 
