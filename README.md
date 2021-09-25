# Jarkom-Modul-1-IUP6-2021


Mukhoram Dimaputra Bagawan 05111942000006 </br>
Fitriana Zahirah Tsabit 05111942000011 </br>
Muhammad Rafi Hayla Arifa 05111942000014 </br>

</br>
</br>

**1. What web server is used on "ichimarumaru.tech"!**
(Mukhoram Dimaputra)

By checking the pcap using filter `http.host ==` we can check the we server information. Our answer is `nginx`. </br>
![1 jarkom](https://user-images.githubusercontent.com/74299958/134666256-af790e60-1622-4d55-8039-7aa90dcdd7fa.png)


**2. Find the packets from the web that use the basic authentication method!**
(Mukhoram Dimaputra)

Using `http.authbasic` in the filter, we could find all the packets.</br>
![2 jarkom](https://user-images.githubusercontent.com/74299958/134666344-66912e30-d2a4-40f2-b832-f03c70c56123.png)

**3. Follow the instructions at basic.ichimaru maru.tech! Username and password can be obtained from the .pcapng file!**
(Mukhoram Dimaputra)

we use `http.authbasic` again here, and by checking the last packet. In the last packet we could check the `Authorization` and open the credentials to get the username and password, which is `kuncimenujulautan` and the pasword is down below. After open the web, we answer the question with our answer.</br>
![3 jarkom](https://user-images.githubusercontent.com/74299958/134666450-461cdcec-3daf-4e6e-96d5-c88e2abfb605.png)
![3 jakom 2](https://user-images.githubusercontent.com/74299958/134666508-0dbcf873-f09e-45cf-a1e9-92d55e56a4b1.png)


**5. Login to portal.ichimarumaru.tech then follow the instructions! The username and password can be obtained from the insert query in the users table from the .pcap file!**
(Mukhoram Dimaputra)

 we search `mysql` in the filter, then open each of the packets. </br>
<img width="956" alt="jarkom 5 1" src="https://user-images.githubusercontent.com/74299958/134769557-8c6f9c9a-7974-4e2c-8732-5ae255434c5a.png">
<img width="942" alt="jarkom 5 2" src="https://user-images.githubusercontent.com/74299958/134769561-0529d902-3e36-4541-bd2b-68a1d59cb434.png">

**6. Find username and password when logging into FTP Server!**
(Fitriana Zahirah)

To find username and password we use `ftp.request.command contains "USER" || ftp.request.command contains "PASS"`</br> 
<img width="956" alt="jarkom 6 1" src="https://user-images.githubusercontent.com/91376801/134772982-1da994ca-262e-46f7-afb6-8ba360c105b8.jpg">

**7. There are 500 zip files saved to FTP Server with names 0.zip, 1.zip, 2.zip, ..., 499.zip. Save and Open the pdf file. (Hint = the name of the pdf is "Real.pdf")**
(Mukhoram Dimaputra)

To find the pdf, we will use `ftp-data contains Real.pdf` in the filter. The filter will show the packet that contains the pdf. After that we click the package then right click it, press follow. Choose TCP stream, then show the data as Raw. Save the file as pdf. </br>
![jarkom 7](https://user-images.githubusercontent.com/74299958/134769335-ebb47a8a-296b-4eac-b29f-e2537f582a7c.png)

**9. From the packets going to FTP, there are indications of storing some files. One of them is a file containing confidential data with the name "secret.zip". Save and open the file!**
(Fitriana Zahirah)

To find the secret.zip we use `ftp-data.command == "STOR secret.zip"`. </br>
There is a 'save' keyword in the question indicating that the file you are looking for can be filtered using the STOR command <\br>
The filter will show the packet that contains the zip. After that we click the package then right click it, press follow. Choose TCP stream, then show the data as Raw. Save the file as zip </br>
<img width="956" alt="jarkom 6 1" src="https://user-images.githubusercontent.com/91376801/134772984-00c0fc4e-6275-45ee-b39d-0353c11389df.jpg">


**10. Also there is "history.txt" which probably contains the history of the bash server! Use the contents of "history.txt" to find the password to open the secret file in "secret.zip"!**
(Fitriana Zahirah)

To find the history.txt we use `ftp-data.command contains "STOR history.txt"`. The filter will show the packet that contains the history.txt. After that we click the package then right click it, press follow. Choose TCP stream, then show the data as ascii.</br>
<img width="956" alt="jarkom 6 1" src="https://user-images.githubusercontent.com/91376801/134772989-4351e7af-d452-462d-9fee-93cfc547011d.jpg">

But we find the history.txt, the program direct to bukanapaapa.txt. so we use the same step `ftp-data.command contains "STOR bukanapaapa.txt"` </br>

<img width="956" alt="jarkom 6 1" src="https://user-images.githubusercontent.com/91376801/134772986-6a57b8fe-904e-4baf-bdea-45ee916a61d7.jpg">

last we find

<img width="956" alt="jarkom 6 1" src="https://user-images.githubusercontent.com/91376801/134772988-88450f1c-fd20-4c3b-9659-7037d0c0e7c0.jpg">


**11.Filter so that wireshark only picks up packets coming from port 80!**
(Muhammad Rafi Hayla)

To picks up packets coming from port 80, we just simply using `tcp.srcport == 80` filter to answer this question. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 35 19" src="https://user-images.githubusercontent.com/74056954/134768452-74761050-0f39-49ac-bfe5-eeccbb8ec29e.png">

**12. Filter so that wireshark only picks up packets containing port 21!**
(Muhammad Rafi Hayla)

In this case, we using `tcp.port == 21 || udp.port == 21` </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 37 29" src="https://user-images.githubusercontent.com/74056954/134768512-ecfd4824-6c63-42f2-992a-03a7255f18cb.png">

**13. Filter so that wireshark only shows packets going to port 443!**
(Muhammad Rafi Hayla)

To shows packets going to port 443, we use `tcp.dstport == 43` filter. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 39 37" src="https://user-images.githubusercontent.com/74056954/134768548-083abd80-62e2-4601-80dc-e943af33c286.png">

**14. Filter so that wireshark only picks up packets going to kemenag.go.id!**
(Muhammad Rafi Hayla)

This time, for picking up the packets going to kemenag.go.id, we use `dst host kemenag.go.id` </br>


<img width="470" alt="Screen Shot 2021-09-25 at 17 42 52" src="https://user-images.githubusercontent.com/74056954/134768636-ebd7ee81-1f1e-4c34-9845-8d743bb94991.png">

**15. Filter so that wireshark only picks up packets coming from your local ip address!**
(Muhammad Rafi Hayla)

First we need to know what is our ip address. Because I'm using MacOs. Here is how I find my ip address; </br>
`System Preferences` > `Network` and `select your connection in the left sidebar`. Then click `Advanced` > `TCP/IP` and you will see your computer’s `IP address` next to IPv4 Address and your router’s IP address next to Router. </br>

Then, we can continue by typing `ip.addr = _you.ip.address_`. </br>

<img width="470" alt="Screen Shot 2021-09-25 at 17 50 15" src="https://user-images.githubusercontent.com/74056954/134768813-f051acec-f68c-4a2a-9a78-9b756dd64e1e.png">

**Our Obstacle**
- In finding the username and password problems, we could not actually find it directly, so we search it manually per packets. </br>
- when donwloading, we actually kinda confused a little bit of how we save it. </br>
- in 11-15, we first confused at what file we use (wi-fi or the pcap files). </br>





