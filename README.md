# ctf-lightbulb-door
Because my memory sucks, here is what we do to beat the lightbulb/door challenge at Hackers Teaching Hackers (HTH).

1. Plug into the network port and run wireshark.
2. Find the IP that is pinging with security in the packet.
3. Set your IP address on your NIC to an IP in the subnet of the device sending the pings.
4. Run an nmap scan of the devices that was sending the pings and include all high ports (previous value was 10.44.120.4:60017)
5. Once you find the port that the website is running on open up a browser and go to it
6. Go to /robots.txt and you will find /users
7. Go to /users and you will find a username and a hash
8. use john or hashcat to crack the hash - password should be chocolate
9. There is also a /images folder that had a clue
10. Enter the username/password to login and turn on the light then get the flag
