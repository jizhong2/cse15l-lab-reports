# Lab Report 2
<br> *Part 1* <br>
<br> Below are screenshots of the code to ChatServer <br>
![Image](webserverpt1.png)
![Image](webserverpt2.png)
<br> Below are two ```/add-message``` on the webserver.
<br> ![Image](webservermsgs)<br>
<br> ![Image](webserver.png) <br>
<br> Method, handleRequest, was called on. <br>
<br> The relevant argument was ```URI url``` and relevant fields are ```String queryString```, ```String[] parameters```, ```String user```, and ```String message```. <br>
<br> ```String queryString``` is dependent on ```URI url```, and ```String[] parameters```, ```String user```, ```String message``` depend on ```String queryString```. Once ```/add-message``` following different queries are added to ```URI url```, it changes the values to ```String[] parameters```, ```String user```, ```String message```, which changes the printed messages on the webserver. <br>
