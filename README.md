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

**3. Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file!**

we use `http.authbasic` again here, and by checking the last packet. In the last packet we could check the `Authorization` and open the credentials to get the username and password, which is `kuncimenujulautan` and the pasword is down below. After open the web, we answer the question with our answer.</br>
![3 jarkom](https://user-images.githubusercontent.com/74299958/134666450-461cdcec-3daf-4e6e-96d5-c88e2abfb605.png)
![3 jakom 2](https://user-images.githubusercontent.com/74299958/134666508-0dbcf873-f09e-45cf-a1e9-92d55e56a4b1.png)


**11.Filter so that wireshark only picks up packets coming from port 80!**

To picks up packets coming from port 80, we just simply using `tcp.srcport == 80` filter to answer this question. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 35 19" src="https://user-images.githubusercontent.com/74056954/134768452-74761050-0f39-49ac-bfe5-eeccbb8ec29e.png">

**12. Filter so that wireshark only picks up packets containing port 21!**

In this case, we using `tcp.port == 21 || udp.port == 21` </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 37 29" src="https://user-images.githubusercontent.com/74056954/134768512-ecfd4824-6c63-42f2-992a-03a7255f18cb.png">

**13. Filter so that wireshark only shows packets going to port 443!**

To shows packets going to port 443, we use `tcp.dstport == 43` filter. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 39 37" src="https://user-images.githubusercontent.com/74056954/134768548-083abd80-62e2-4601-80dc-e943af33c286.png">

**14. Filter so that wireshark only picks up packets going to kemenag.go.id!**

This time, for picking up the packets going to kemenag.go.id, we use `dst host kemenag.go.id` </br>


<img width="470" alt="Screen Shot 2021-09-25 at 17 42 52" src="https://user-images.githubusercontent.com/74056954/134768636-ebd7ee81-1f1e-4c34-9845-8d743bb94991.png">

**15. Filter so that wireshark only picks up packets coming from your local ip address!**

First we need to know what is our ip address. Because I'm using MacOs. Here is how I find my ip address; </br>
`System Preferences` > `Network` and `select your connection in the left sidebar`. Then click `Advanced` > `TCP/IP` and you will see your computer’s `IP address` next to IPv4 Address and your router’s IP address next to Router. </br>

Then, we can continue by typing `ip.addr = _you.ip.address_`. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 50 15" src="https://user-images.githubusercontent.com/74056954/134768813-f051acec-f68c-4a2a-9a78-9b756dd64e1e.png">





