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




