# Fake-Game-Website-Attack
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

cd, into the metasploit directory, then nano into the config.yaml file


<img width="2530" height="1068" alt="Screenshot 2025-08-26 162501" src="https://github.com/user-attachments/assets/f4a37f47-ddcb-47cd-8974-952fac17ad6a" />

In the Config.yaml file there are three things to do
1. Change the Host from your VM to your server IP
2. Change the callback Host to your server IP
3. Create a custom path at the bottom '/usr/share/metasploit-framework/'










