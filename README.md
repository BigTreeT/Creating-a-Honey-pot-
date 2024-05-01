In this project I will be creating a honey pot in an ubuntu machine using the cowrie Python virtual environment framework 

First things first install the virtual environment package from python, next we clone the cowrie program from github to our directory 

We will now activate our python virtual environment where cowrie will operate in with its own fake filesystem that logs and actually has a playback system to watch what occured with every breach incident 

![Installing cowry VM](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/7496959f-ef77-444a-8c06-3eb4d8b41b49)

Cowrie comes with a default user that attackers may recognize so we will need to go into our config files and change it to something more enticing 

![changing the username in cowry](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/dcd46d44-3375-4d61-95b4-e111845dd6d7)

Next we will ensure that any requests to port 22 will be forwarded to port 2222 to our honeypot 

![ip rerouting to honey pot](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/7afa5ab6-5afd-4318-b698-45e5080b71fd)

We will make sure port 22 is enabled on our machine and ensure cowrie is also accepting ssh traffic

![SSH is enabled by default but to make sure](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/81309587-6cba-4303-97ad-9c2c4ff80e55)
![Screenshot from 2024-04-30 19-16-38](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/81d4e495-097e-4f84-89b8-28a10ce250b3)

To add an extra layer of protection cowrie has the option to take advantage of Abusedipdb which scans for known malicious ips and reports them. We will use our given api key to enable this feature 

![Screenshot from 2024-04-30 19-01-23](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/95f79527-756b-4b6a-9eb3-3a3dc605ef55)
![Screenshot from 2024-04-30 18-55-47](https://github.com/BigTreeT/Creating-a-Honey-pot-/assets/157978941/fbdd9af1-b5a2-49fc-b4ba-4a2011cfb6db)

As long as the virtual environment is active our cowrie honeypot will be functional


