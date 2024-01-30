# Lab Report 2
<br> *Part 1* <br>
<br> Below are screenshots of ```/add-message``` <br>
<br> Method, handleRequest, was called on. <br>
<br> The relevant argument was ```URI url``` and relevant fields are ```String queryString```, ```String[] parameters```, ```String user```, and ```String message```. <br>
<br> ```String queryString``` is dependent on ```URI url```, and ```String[] parameters```, ```String user```, ```String message``` depend on ```String queryString```. Once ```/add-message``` following different queries are added to ```URI url```, it changes the values to ```String[] parameters```, ```String user```, ```String message```, which changes the printed messages on the webserver. <br>
