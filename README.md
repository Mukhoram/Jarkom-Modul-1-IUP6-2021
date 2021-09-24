# Jarkom-Modul-1-IUP6-2021


Mukhoram Dimaputra Bagawan 05111942000006 </br>
Fitriana Zahirah Tsabit 05111942000011 </br>
Muhammad Rafi Hayla Arifa 05111942000014 </br>

</br>
</br>

**1. What web server is used on "ichimarumaru.tech"!**

By checking the pcap using filter `http.host ==` we can check the we server information. Our answer is `nginx`.

**2. Find the packets from the web that use the basic authentication method!**

Using `http.authbasic` in the filter, we could find all the packets.

**3.Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file!**

we use `http.authbasic` again here, and by checking the last packet. In the last packet we could check the `Authorization` and open the credentials to get the username and password, which is `kuncimenujulautan` and the pasword is down below. After open the web, we answer the question with our answer.





