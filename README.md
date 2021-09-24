# Jarkom-Modul-1-IUP6-2021


Mukhoram Dimaputra Bagawan 05111942000006 </br>
Fitriana Zahirah Tsabit 05111942000011 </br>
Muhammad Rafi Hayla Arifa 05111942000014 </br>

</br>
</br>

**1. What web server is used on "ichimarumaru.tech"!**

By checking the pcap using filter `http.host ==` we can check the we server information. Our answer is `nginx`. </br>
![1 jarkom](https://user-images.githubusercontent.com/74299958/134666256-af790e60-1622-4d55-8039-7aa90dcdd7fa.png)


**2. Find the packets from the web that use the basic authentication method!**

Using `http.authbasic` in the filter, we could find all the packets.</br>
![2 jarkom](https://user-images.githubusercontent.com/74299958/134666344-66912e30-d2a4-40f2-b832-f03c70c56123.png)

**3.Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file!**

we use `http.authbasic` again here, and by checking the last packet. In the last packet we could check the `Authorization` and open the credentials to get the username and password, which is `kuncimenujulautan` and the pasword is down below. After open the web, we answer the question with our answer.</br>
![3 jarkom](https://user-images.githubusercontent.com/74299958/134666450-461cdcec-3daf-4e6e-96d5-c88e2abfb605.png)
![3 jakom 2](https://user-images.githubusercontent.com/74299958/134666508-0dbcf873-f09e-45cf-a1e9-92d55e56a4b1.png)





